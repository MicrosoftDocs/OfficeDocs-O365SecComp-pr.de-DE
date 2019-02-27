---
title: Suchstatistiken
ms.author: markjjo
author: esclee
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
ms.openlocfilehash: a2234d0a0e94e3fbb15f8fac8f6e49cc7b26cfb2
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295658"
---
# <a name="search-statistics"></a>Suchstatistiken

Sie können Ihre Suchergebnisse auf eine Weise überprüfen, indem Sie sich die Statistiken rund um Ihre Ergebnisse ansehen, um sicherzustellen, dass Sie Ihren Erwartungen entsprechen. Wenn eine Suche abgeschlossen ist, werden allgemeine Statistiken im Such Detail Flyout angezeigt:
- Anzahl und Umfang der von der Suche abgerufenen Elemente
- Anzahl und Volumen von teilweise indizierten/nicht indizierten Elementen, die in den Suchspeicherorten gefunden wurden
- Anzahl der durchsuchten Postfächer und Speicherorte. Um detailliertere Statistiken anzuzeigen, klicken Sie im Such Detail Flyout auf "Statistiken".

## <a name="summary"></a>Zusammenfassung

In der Zusammenfassungsansicht können die Suchergebnisse nach Standorttyp aufgeschlüsselt angezeigt werden (beispielsweise Exchange). Für jeden Standorttyp können Sie Folgendes sehen:
- Anzahl der Standorte mit Elementen, die den Suchbedingungen entsprechen
- Anzahl der Elemente aus diesen Speicherorten, die den Suchbedingungen entsprechen
- Gesamtvolumen der Elemente, die den Suchbedingungen entsprechen.

## <a name="top-locations"></a>Top-Standorte

In der Ansicht der oberen Speicherorte werden die einzelnen Standorte mit den meisten Treffern angezeigt. Für jeden Standort wird Folgendes angezeigt:
- Speicherort Name (z. b. SharePoint-URL)
- Typ des Speicherorts
- Anzahl der Elemente, die den Suchbedingungen entsprechen
- Gesamtvolumen der Elemente, die den Suchbedingungen entsprechen.

## <a name="queries"></a>Abfragen

Wenn Sie in Ihrer Abfrage (c:s) Schlüsselwort-oder Stichwort Zeilen verwendet haben, können Sie den aufschlüsseln der Abfrage in der Ansicht Abfragen pro Standorttyp erkennen. Für jeden Standorttyp wird Folgendes angezeigt:

- Bauteil: Diese Spalte hat entweder das Wort "Primary" oder "Schlüsselwort". "Primary" bedeutet, dass die Zeile Statistiken über die gesamte Abfrage enthält, wohingegen "Keyword" eine der Abfragekomponenten bedeutet.

- Query: die tatsächliche Abfragekomponente, auf die sich die Zeile bezieht. Wenn der Webpart "Primary" ist, handelt es sich um die gesamte Abfrage. Wenn Teil "Schlüsselwort" war, wird eine der Abfragekomponenten hier angezeigt.
  
  - Wenn Sie alle Inhalte in Postfächern Durchsuchen (ohne Schlüsselwörter anzugeben), lautet die tatsächliche Abfrage (Größe > = 0), sodass alle Elemente zurückgegeben werden.
  
  - Beim Durchsuchen von SharePoint Online-und OneDrive für Business-Websites werden die beiden folgenden Komponenten hinzugefügt:
    
    - NICHT IsExternalContent: 1-schließt Inhalte aus einer lokalen SharePoint-Organisation aus
    
    - NICHT isOneNotePage: 1-schließt alle OneNote-Dateien aus, da es sich dabei um Duplikate eines Dokuments handeln würde, das mit der Suchabfrage übereinstimmt.

- Anzahl der Standorte mit Elementen, die den Suchbedingungen entsprechen.

- Die Anzahl der Elemente aus diesen Speicherorten, die den Suchbedingungen entsprechen.

- Gesamtvolumen der Elemente, die den Suchbedingungen entsprechen.