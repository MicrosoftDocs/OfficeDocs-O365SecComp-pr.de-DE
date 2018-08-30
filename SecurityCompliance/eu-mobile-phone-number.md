---
title: EU Mobiltelefonnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der EU Mobiltelefonnummer vertraulichen Informationen.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529356"
---
# <a name="eu-mobile-phone-number"></a>EU Mobiltelefonnummer

Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der EU Mobiltelefonnummer vertraulichen Informationen. 
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Ziffern ohne standard Längen
  
### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_austria_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_austria_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_austria_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a>Belgien

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_belgium_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_belgium_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_belgium_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a>Bulgarien

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_bulgaria_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_bulgaria_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_bulgaria_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a>Kroatien

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_croatia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_croatia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_croatia_eu_mobile_number` gefunden wird. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a>Zypern

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_cyprus_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_cyprus_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_cyprus_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a>Tschechische Republik

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_czech_republic_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_czech_republic_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_czech_republic_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a>Dänemark

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_denmark_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_denmark_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_denmark_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a>Estland

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_estonia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_estonia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_estonia_eu_mobile_number` gefunden wird. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a>Finnland

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_finland_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_finland_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_finland_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a>Frankreich

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_france_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_france_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_france_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a>Deutschland

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_germany_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_germany_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_germany_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a>Griechenland

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_greece_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_greece_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_greece_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a>Ungarn

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_hungary_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_hungary_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_hungary_eu_mobile_number` gefunden wird. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a>Irland

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_ireland_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_ireland_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_ireland_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a>Italien

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_italy_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_italy_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_italy_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a>Lettland

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_latvia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_latvia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_latvia_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a>Litauen

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_lithuania_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_lithuania_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_lithuania_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a>Luxemburg

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_luxumburg_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_luxumburg_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_luxumburg_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a>Malta

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_malta_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_malta_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a>Niederlande

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_netherlands_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_netherlands_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_netherlands_eu_mobile_number` gefunden wird. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a>Polen

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_poland_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_poland_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_poland_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a>Portugal

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_portugal_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_portugal_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_portugal_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a>Rumänien

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_romania_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_romania_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_romania_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a>Slowakei

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovakia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_slovakia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovakia_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a>Slowenien

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovenia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_slovenia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovenia_eu_mobile_number` gefunden wird. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a>Spanien

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_spain_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_spain_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_spain_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a>Schweden

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_sweden_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_sweden_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_sweden_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a>GROßBRITANNIEN

### <a name="pattern"></a>Muster

-  Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_uk_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Der reguläre Ausdruck `Regex_uk_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_uk_eu_mobile_number` gefunden wird. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

