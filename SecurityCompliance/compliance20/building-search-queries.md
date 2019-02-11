---
title: Erstellen von Suchabfragen
ms.author: markjjo
author: markjjo
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
ms.openlocfilehash: c337b49491fca11e0ba5bc13d22ac3e54038c400
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695071"
---
# <a name="build-search-queries"></a>Erstellen von Suchabfragen

In der Abfrage erstellen, können Sie verschiedene Schlüsselwörter und Bedingungen um zu definieren, welche Elemente gefunden verwenden.

## <a name="keyword-searches"></a>Schlüsselwortsuchen

Geben Sie im Feld **Stichwörter** eine Suchabfrage. Sie können angeben, Schlüsselwörter, Nachricht Eigenschaften wie gesendet und empfangen, Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, das ein Dokument zuletzt geändert wurde. Sie können eine komplexere Abfragen verwenden, die einen booleschen Operators, wie **AND**, **OR**, **nicht**und **NEAR**verwenden. Sie können auch suchen für vertrauliche Informationen (wie Sozialversicherungsnummern) in Dokumenten, oder suchen Sie nach Dokumenten, die extern freigegeben haben. Wenn Sie das Schlüsselwort Feld leer lassen, werden alle Inhalte, die in der angegebenen Speicherorte für Inhalte befindet sich in den Suchergebnissen enthalten sein.
    
Alternativ können Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** und den Typ ein Schlüsselworts in jede Zeile klicken. Wenn Sie dies tun, sind die Schlüsselwörter für jede Zeile ein logischer Operator ( **C:s**) vorhanden, die Funktionalität der **OR** -Operator in der Suchabfrage ähnlich ist, die erstellt wird. 
    
Gründe für die Verwendung der Schlüsselwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente jedes Schlüsselwort überein. Dadurch können Sie schnell erkennen, welche Schlüsselwörter der am häufigsten (und mindestens) wirksam werden. Sie können auch eine Stichwortbegriff (in Klammern eingeschlossen sind) in einer Zeile. Weitere Informationen zu Suchstatistik finden Sie unter [Search-Statistik](search-statistics.md).

## <a name="conditions"></a>Bedingungen
    
Sie können die Suchkriterien, um eine Suche einzugrenzen und eine genauere Ergebnisse zurückgeben hinzufügen. Jede Bedingung hinzugefügt Search-Abfrage, die erstellt und ausgeführt werden, wenn Sie die Suche starten eine-Klausel. Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) durch einen logischen Operator (**c: c**) verbunden, die an den **und** -Operator vergleichbar ist. Dies bedeutet, dass Elemente erfüllen der Stichwortabfrage und einen oder mehrere Bedingungen, die in den Ergebnissen berücksichtigt werden müssen. Dies ist die Bedingungen wie helfen, um Ihre Suchergebnisse einzuschränken. Eine Liste und eine Beschreibung der Bedingungen, die Sie bei einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchen Conditions" in [Stichwortabfragen und Suchkriterien für die Inhaltssuche](../keyword-queries-and-search-conditions.md#search-conditions).


