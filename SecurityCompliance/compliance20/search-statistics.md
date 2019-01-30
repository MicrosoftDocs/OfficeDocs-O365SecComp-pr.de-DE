---
title: Suchstatistik
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
ms.openlocfilehash: c5b7caff3550d42d84408d6b4e966655b8341123
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607816"
---
# <a name="search-statistics"></a>Suchstatistik
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
- Anzahl von Standorten, die Elemente, die die Suchkriterien entsprechen.
- Anzahl von Elementen aus dieser Speicherorte, die die Suchkriterien entsprechen.
- Insgesamt Volumne von Elementen, die die Suchkriterien entsprechen.

## <a name="refiners"></a>Einschränkungen
Für eine Exchange-Postfächer kann Einschränkungen Ansicht zusätzliche Abstürzen von ItemClass, Absender und Empfänger. Für jeden Wert, Speicherort und Einschränkung sehen Sie, wie viele Dokumente in die Suche zurückgegeben wurden.