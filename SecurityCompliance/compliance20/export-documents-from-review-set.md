---
title: Exportieren von Dokumenten aus einem Übersichts Satz
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
ms.openlocfilehash: ea9db6d95b003b5a741ae8a235fc5f06087f87d6
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527180"
---
# <a name="export-documents-from-a-review-set"></a>Exportieren von Dokumenten aus einem Übersichts Satz

Das Exportieren von Inhalten aus einem Übersichts Satz kann über drei verschiedene Methoden erfolgen:

## <a name="download"></a>Download

Download bietet eine einfache Möglichkeit zum Herunterladen von Inhalten aus einem Übersichts Satz im systemeigenen Format. Es nutzt die Datentransfer Funktionen des Browsers, sodass eine Browser Ansage angezeigt wird, sobald ein Download bereit ist. Dateien, die mit dieser Methode heruntergeladen werden, werden in eine Containerdatei gepackt und sind Dateien auf Elementebene. Wenn Sie eine Anlage auswählen, erhalten Sie daher automatisch eine e-Mail mit der enthaltenen Anlage. Wenn Sie eine Excel-Kalkulationstabelle auswählen, die in ein Word-Dokument eingebettet wurde, erhalten Sie auch das Word-Dokument mit der eingebetteten Excel-Kalkulationstabelle. Heruntergeladene Elemente behalten das Datum der letzten Änderung bei, das als Dateieigenschaft angezeigt werden kann.

Um Inhalte aus einem Übersichts Satz herunterzuladen, wählen Sie zunächst die Dateien aus, die Sie herunterladen möchten, und klicken Sie dann im Menü Aktionen auf "herunterladen".

![Screenshot einer Computerbeschreibung, die automatisch generiert wird](../media/eDiscoDownload.png)

## <a name="export"></a>Exportieren

Der Export ermöglicht Benutzern das Anpassen der Inhalte, die im Downloadpaket enthalten sind. Es bietet eine Konfigurationsseite mit den folgenden Einstellungen:

### <a name="metadata-file"></a>Metadatendatei

> Dies kann als ihre "Datei laden" angesehen werden, die Metadaten enthält, die mit den exportierten Dateien verknüpft sind. Eine Liste der Felder, die in der Metadatendatei zur \[Verfügung stehen, finden Sie unter Link\]. Diese Datei kann i. d. r. von 3<sup>RD</sup> -Anbieter Tools nachgeschaltet werden.

### <a name="tag-data"></a>Tag-Daten

> Dieser Inhalt würde als Felder in der Metadatendatei hinzugefügt werden. Sie enthält alle Tag-Informationen, die in Übersichts Sätzen angewendet wurden.

### <a name="text-files"></a>Textdateien

> Für jede aus einem Übersichts Satz exportierte Datei können Text Dateien generiert werden. Häufig werden diese Dateien von den Dienst Partnern im Rahmen der Einnahme von Daten in 3 Dritt<sup></sup> Anbieter Tools (Downstream) benötigt.

### <a name="redacted-files"></a>Gehandelte Dateien

> Wenn während der Überprüfungen redigierte PDFs generiert werden, sind diese Dateien während des Exports verfügbar. Benutzer können entscheiden, ob Sie nur systemeigene Dateien exportieren oder natives ersetzen möchten, die mit den gebrannten PDFs in der PDF-Datei ausgeführt wurden.

### <a name="export-location"></a>Exportspeicherort

> Exportierte Inhalte werden entweder an ein von Microsoft bereitgestelltes Azure-BLOB oder an ein Kunden-BLOB übermittelt, wenn die Details beim Export bereitgestellt werden.

## <a name="export-structure"></a>Export Struktur

Wenn Inhalte aus einem Übersichts Satz exportiert werden, wird der Inhalt in der folgenden Struktur organisiert.

  - Stammordner – Download-ID
    
      - Export\_laden\_Datei. CSV = Metadatendatei
    
      - Summary. txt = eine Zusammenfassungsdatei mit Export Statistiken
    
      - Eingabe\_-oder\_systemeigene Dateien = enthält alle systemeigenen Dateien
    
      - Error\_files = enthält alle Fehler Dateien, die im Export enthalten sind
        
          - ExtractionError – eine CSV-Datei, die alle verfügbaren Metadaten von Dateien enthält, die nicht ordnungsgemäß aus übergeordneten Dateien extrahiert wurden
        
          - ProcessingError – Inhalte mit Verarbeitungsfehlern. Dieser Inhalt ist auf Elementebene Bedeutung wenn bei einer Anlage ein Verarbeitungsfehler auftritt, wird die e-Mail mit der Anlage in diesen Ordner aufgenommen.
    
      - Extrahierte\_Text\_Dateien = enthält alle extrahierten Textdateien, die bei der Verarbeitung generiert wurden.

## <a name="review-set"></a>Übersichts Satz

Inhalte können zu einem anderen Übersichts Satz hinzugefügt werden.