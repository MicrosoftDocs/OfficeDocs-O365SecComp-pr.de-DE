---
title: Suchstatistiken
ms.author: markjjo
author: esclee
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 0cfc1e5f04887cbdbcc0be8854fc50d6f9b5f1f2
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706006"
---
# <a name="search-statistics"></a>Suchstatistiken

Eine Möglichkeit, Sie können die Suchergebnisse überprüfen können ist, sehen Sie sich die Statistiken, um die Ergebnisse, um sicherzustellen, dass sie die gewünschte ausgerichtet. Wenn eine Suche abgeschlossen ist, sind allgemeine Statistiken für die Suche Details flyoutmenü aufgeführt:
- Anzahl und Volumen der Elemente abgerufen, die von der Suche
- Anzahl und Menge der indiziert/nicht indizierten teilweise Elemente, die in der Suche gefunden wurden
- Anzahl der Postfächer und Speicherorte durchsucht. Um eine detaillierte Statistik anzuzeigen, klicken Sie auf "Statistik" aus der Suche Details flyoutmenü.

## <a name="summary"></a>Zusammenfassung

In der Ansicht "Zusammenfassung" können Sie die Suchergebnisse, aufgeschlüsselt nach Typ des Speicherorts (z. B. Exchange) finden Sie unter. Für jeden Standort sehen Sie:
- Anzahl von Standorten, die Elemente, die die Suchkriterien entsprechen.
- Anzahl von Elementen aus dieser Speicherorte, die die Suchkriterien entsprechen.
- Gesamtvolumen der Elemente, die die Suchkriterien entsprechen.

## <a name="top-locations"></a>Obere Speicherorte

In der oberen Speicherorte Ansicht finden Sie unter den einzelnen Standorten mit die meisten Übereinstimmungen. Für jeden Standort sehen Sie:
- Name des Standorts (z. B. SharePoint-URL)
- Typ des Speicherorts
- Anzahl der Elemente, die die Suchkriterien entsprechen.
- Gesamtvolumen der Elemente, die die Suchkriterien entsprechen.

## <a name="queries"></a>Abfragen

Wenn Sie (C:s) Schlüsselwort oder Schlüsselwort Zeilen in der Abfrage verwendet haben, können Sie die Aufschlüsselung der Abfrage in der Ansicht "Abfragen" pro Speicherorttyp sehen. Für jeden Standort sehen Sie:

- Teil: Diese Spalte wird entweder das Wort "Primary" oder "Schlüsselwort" haben. "Primary" bedeutet, dass die Zeile Statistiken auf die gesamte Abfrage darstellt, während "Schlüsselwort" eine der Abfragekomponenten bedeutet.

- Abfrage: die tatsächlichen Abfragekomponente verweist auf die Zeile. Wenn "Primary" gehört, wird dadurch der gesamten Abfrage; Wenn Teil "Schlüsselwort" war, sehen Sie eine der hier die Abfragekomponenten.
  
  - Wenn Sie alle InhaltKontextabhängiges Postfächer (durch Angabe keine Schlüsselwörter) suchen, ist die eigentliche Abfrage (Größe > = 0), damit alle Elemente zurückgegeben werden
  
  - Wenn Sie SharePoint Online und OneDrive for Business-Websites suchen, werden die beiden folgenden Komponenten hinzugefügt:
    
    - NICHT IsExternalContent:1 - schließt alle Inhalte aus einer lokalen SharePoint-Organisation
    
    - NICHT IsOneNotePage: 1 - schließt alle OneNote-Dateien, da diese Duplikate eines beliebigen Dokuments wäre, die mit die Suchabfrage übereinstimmt.

- Anzahl der Standorte, die Elemente hatte, die die Suchkriterien entsprechen.

- Die Anzahl von Elementen aus dieser Speicherorte, die die Suchkriterien entsprechen.

- Gesamtvolumen der Elemente, die die Suchkriterien entsprechen.

## <a name="refiners"></a>Einschränkungen

Für eine Exchange-Postfächer kann Einschränkungen Ansicht zusätzliche Abstürzen von ItemClass, Absender und Empfänger. Für jeden Wert, Speicherort und Einschränkung sehen Sie, wie viele Dokumente in die Suche zurückgegeben wurden.