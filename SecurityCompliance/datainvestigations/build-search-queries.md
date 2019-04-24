---
title: Erstellen von Suchabfragen
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
description: Verwenden Sie Stichwörter und Bedingungen, um den Suchbereich bei der Suche nach Daten einzuschränken, wenn Sie die Datenermittlung in Microsoft 365 verwenden.
ms.openlocfilehash: eeca1bf7ff89d1b7f79ceeed3334668e354f035a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262887"
---
# <a name="build-search-queries"></a>Erstellen von Suchabfragen

Beim Erstellen von Suchabfragen können Sie Schlüsselwörter verwenden, um bestimmte Inhalte und Bedingungen zu finden, um den Umfang der Suche einzuschränken, um Elemente zurückzugeben, die für Ihre Untersuchung am relevantesten sind.

![Verwenden von Schlüsselwörtern und Bedingungen zum Einschränken der Ergebnisse einer Suche](../media/SearchQueryBox.png)

## <a name="keyword-searches"></a>Stichwortsuche

Geben Sie eine Stichwortabfrage in das Feld **Schlüsselwörter** in der Suchabfrage ein. Sie können Schlüsselwörter, e-Mail-Nachrichteneigenschaften (beispielsweise gesendete und empfangene Datumsangaben) oder Dokumenteigenschaften (wie Dateinamen oder das Datum, an dem ein Dokument zuletzt geändert wurde) angeben. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**. Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Dokumenten in SharePoint und OneDrive (nicht in e-Mail-Nachrichten) suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Feld **Schlüsselwörter** leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in die Suchergebnisse eingeschlossen.
    
Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Schlüsselwort oder ein Stichwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch einen logischen Operator (der als *c:s*dargestellt wird) verbunden, der in der Funktionalität mit dem **or** -Operator in der erstellten Suchabfrage vergleichbar ist. Dies führt dazu, dass Elemente, die ein Schlüsselwort in einer beliebigen Zeile enthalten, in den Suchergebnissen enthalten sind.

![Verwenden der Stichwortliste zum Abrufen von Statistiken zu jedem Schlüsselwort in der Abfrage](../media/KeywordListSearch.png)

Gründe für die Verwendung der Keyword-Liste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit jedem Stichwort in der Keyword-Liste übereinstimmen. Auf diese Weise können Sie schnell die Schlüsselwörter identifizieren, die am meisten (und am wenigsten) effektiv sind. Sie können auch eine Schlüsselwortphrase (umgeben von Klammern) in einer Zeile in der Stichwörter Liste verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistiken](search-statistics.md).

> [!NOTE]
> Um Probleme zu vermeiden, die durch umfangreiche Stichwortlisten verursacht werden, können Sie in der Keyword-Liste maximal 20 Zeilen eingeben.

## <a name="conditions"></a>Bedingungen
    
Sie können Suchbedingungen hinzufügen, um den Bereich einer Suche einzuschränken und eine verfeinerte Reihe von Ergebnissen zurückzugeben. Jede Bedingung fügt eine Klausel zu der Suchabfrage hinzu, die erstellt und beim Starten der Suche ausgeführt wird. Eine Bedingung ist logisch mit der Stichwortabfrage (angegeben im Stichwortfeld) durch einen logischen Operator (der als *c:c*dargestellt wird) verbunden, der in der Funktionalität mit dem **and-** Operator vergleichbar ist. Dies führt dazu, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in die Suchergebnisse eingeschlossen werden sollen. Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen. Eine Liste und Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" in [Stichwortabfragen und Suchbedingungen](../keyword-queries-and-search-conditions.md#search-conditions).
