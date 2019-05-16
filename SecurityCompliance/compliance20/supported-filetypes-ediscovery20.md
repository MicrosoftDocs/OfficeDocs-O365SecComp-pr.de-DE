---
title: Unterstützte Dateitypen in Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d8e9689cb04929137787225579dcda17005c8bfe
ms.sourcegitcommit: 7be8617ce75909f0fa1a2f6e72749e2ef4bb2d3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2019
ms.locfileid: "34088808"
---
# <a name="supported-file-types-in-advanced-ediscovery"></a>Unterstützte Dateitypen in Advanced eDiscovery

Advanced eDiscovery unterstützt viele Dateitypen für viele verschiedene Ebenen, die in der folgenden Tabelle beschrieben werden. Diese Liste ist nicht abgeschlossen, und wir werden neue Dateitypen hinzufügen, während wir unsere Validierungstests fortsetzen. Die Tabellen geben an, ob ein Dateityp für die Textextraktion (OCR für Bilder) unterstützt wird, der in der systemeigenen Anzeige angezeigt werden kann, und unterstützt auch den Kommentar Betrachter in Advanced eDiscovery.

## <a name="archive--container"></a>Archiv/Container

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Container Extraktion | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |
| Application/x-7z-Compressed | Ja | Ja | Ja | .7z |
| Anwendung/x-rar-komprimiert | Ja | Ja | Ja | . rar |
| Anwendung/x-tar | Ja | Ja | Ja | . tar |
| Anwendung/zip | Ja | Ja | Ja | . zip |
||||||||

## <a name="database"></a>Datenbank

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| Application/x-Msaccess | Ja | Ja | Ja | Nein | Nein | . mdb |
||||||||

## <a name="email"></a>E-Mail

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-Outlook | Ja | Ja | Ja | Ja | Ja | . msg |
| Nachricht/RFC822 | Ja | Ja | Ja | Ja | Ja | . eml |
| Text/vCard-Kontakt | Ja | Ja | Ja | Ja | Ja | . vcf |
||||||||

## <a name="email-container"></a>E-Mail-Container

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Container Extraktion | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |
| Application/mbox | Ja | Ja | Ja | . mbox |
| application/vnd. MS-Outlook-PST | Ja | Ja | Ja | PST |
||||||||

## <a name="html"></a>HTML

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| Application/XHTML + XML | Ja | Ja | Ja | Ja | Ja | . XHTML |
| Anwendung/XML | Ja | Ja | Ja | Ja | Ja | . XML |
| Text/HTML | Ja | Ja | Ja | Ja | Ja | . htm;. html;. shtml |
||||||||

## <a name="image"></a>Image

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | OCR-Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| Bild/BMP | Ja | Ja | Ja | Ja | Ja | BMP |
| Image/EMF | Ja | Ja | Ja | Ja | Ja | . EMF |
| image/gif | Ja | Ja | Ja | Ja | Ja | .gif |
| image/jpeg | Ja | Ja | Ja | Ja | Ja | . JPEG;. jpg |
| image/png | Ja | Ja | Ja | Ja | Ja | .png |
| Image/SVG + XML | Ja | Ja | Ja | Ja | Nein | . svg |
| Bild/TIFF | Ja | Ja | Ja | Ja | Ja | . TIF |
| Image/vnd. DWG | Ja | Ja | Ja | Ja | Ja | . dwg;. DXF |
| Image/WMF | Ja | Ja | Ja | Ja | Ja | . WMF |
||||||||

## <a name="microsoft-excel"></a>Microsoft Excel

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-Excel | Ja | Ja | Ja | Ja | Ja | . dat;. xls |
| application/vnd. MS-Excel. Sheet. Binary. macroenabled. 12 | Ja | Ja | Ja | Ja | Nein | . xlsb |
| application/vnd. MS-Excel. Sheet. macroenabled. 12 | Ja | Ja | Ja | Ja | Ja | . xlsm |
| application/vnd. MS-Excel. Template. macroenabled. 12 | Ja | Ja | Ja | Nein | Nein | . xltm |
| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet | Ja | Ja | Ja | Ja | Ja | . xlsx |
| application/vnd. openxmlformats-officeDocument. SpreadsheetML. Template | Ja | Ja | Ja | Ja | Ja | . xltx |
||||||||

## <a name="microsoft-powerpoint"></a>Microsoft Powerpoint

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-PowerPoint | Ja | Ja | Ja | Ja | Ja | . Pot;. PPS;. ppt |
| application/vnd.openxmlformats-officedocument.presentationml.presentation | Ja | Ja | Ja | Ja | Ja | PPTX |
| application/vnd. openxmlformats-officeDocument. PresentationML. Slideshow | Ja | Ja | Ja | Ja | Ja | . ppsx |
| application/vnd. openxmlformats-officeDocument. PresentationML. Template | Ja | Ja | Ja | Ja | Ja | . POTX |
||||||||

## <a name="microsoft-publisher"></a>Microsoft Publisher

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| Application/x-mspublisher | Ja | Ja | Ja | Ja | Ja | . pub |
||||||||

## <a name="microsoft-visio"></a>Microsoft Visio

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-Visio. Drawing | Ja | Ja | Ja | Ja | Nein |  |
| application/vnd. Visio | Ja | Ja | Ja | Ja | Ja | . vsd |
||||||||

## <a name="microsoft-word"></a>Microsoft Word

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/msword | Ja | Ja | Ja | Ja | Ja | . dat;. doc |
| Anwendung/RTF | Ja | Ja | Ja | Ja | Ja | . doc;. RTF |
| application/vnd. MS-Word. Document. macroenabled. 12 | Ja | Ja | Ja | Ja | Ja | DOCM |
| application/vnd. MS-Word. Template. macroenabled. 12 | Ja | Ja | Ja | Ja | Ja | . dotm |
| application/vnd.openxmlformats-officedocument.wordprocessingml.document | Ja | Ja | Ja | Ja | Ja | DOCX |
| application/vnd. openxmlformats-officeDocument. WordprocessingML. Template | Ja | Ja | Ja | Ja | Ja | . dotx |
||||||||

## <a name="microsoft-works"></a>Microsoft Works

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. MS-Works-SS | Ja | Ja | Nein | Nein | Nein | . WPS |
| application/vnd. MS-Works-WP | Ja | Ja | Nein | Nein | Nein | . WPS |
||||||||

## <a name="open-document-format"></a>Dokument Format öffnen

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. Oasis. OpenDocument. Text | Ja | Ja | Ja | Ja | Ja | . ODT |
||||||||

## <a name="other"></a>Andere

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/json | Ja | Ja | Ja | Ja | Ja | n/v |
| application/vnd. MS-Graph | Ja | Ja | Nein | Nein | Nein |  |
| Anwendung/winhlp | Ja | Ja | Nein | Nein | Nein | . hlp |
| Application/x-TNEF | Ja | Ja | Nein | Nein | Nein |  |
||||||||

## <a name="plain-text"></a>Nur-Text

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| Text/CSV | Ja | Ja | Ja | Ja | Ja | . CSV |
| text/plain | Ja | Ja | Ja | Ja | Ja | . con;. CSS;. CSV;. dat;. pl;. txt |
||||||||

## <a name="portable-document-format"></a>Portable Document Format

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/pdf | Ja | Ja | Ja | Ja | Ja | .pdf |
||||||||

## <a name="word-perfect"></a>Word Perfect

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. WordPerfect; Version = 5.0 | Ja | Ja | Ja | Nein | Nein | . WPD |
| application/vnd. WordPerfect; Version = 5.1 | Ja | Ja | Ja | Nein | Nein | . WPD |
| application/vnd. WordPerfect; Version = 6. x | Ja | Ja | Ja | Nein | Nein | . WPD |
||||||||

## <a name="word-pro"></a>Word pro

| MIME-Typ | Datei Identifizierung | Extrahieren von Metadaten | Text Extraktion | Native Viewer | Betrachter mit Anmerkungen versehen | Mögliche Erweiterungen |
| :- |  :- |  :- |  :- |  :- |  :- |  :- |
| application/vnd. Lotus-WordPro | Ja | Ja | Nein | Nein | Nein | . LWP |
||||||||
