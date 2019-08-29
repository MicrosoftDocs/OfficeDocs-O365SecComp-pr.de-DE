---
title: Erstellen von Suchabfragen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Verwenden Sie Stichwörter und Bedingungen, um den Suchbereich bei der Suche nach Daten zu beschränken, wenn Sie die Datenermittlung in Microsoft 365 verwenden.
ms.openlocfilehash: 913306ff488d9cf2ba715c26eaa49f6f8e1473aa
ms.sourcegitcommit: 3962de88a143f0eb416b5cfdfd777d731f560ec8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2019
ms.locfileid: "36649940"
---
# <a name="build-search-queries"></a>Erstellen von Suchabfragen

Beim Erstellen von Suchabfragen können Sie Schlüsselwörter verwenden, um bestimmte Inhalte und Bedingungen zu finden, um den Umfang der Suche einzuschränken, um Elemente zurückzugeben, die für Ihre Untersuchung am relevantesten sind.

![Verwenden von Stichwörtern und Bedingungen zum Einschränken der Ergebnisse einer Suche](../media/SearchQueryBox.png)

## <a name="keyword-searches"></a>Stichwortsuche

Geben Sie eine Stichwortabfrage in das Feld **Schlüsselwörter** in der Suchabfrage ein. Sie können Schlüsselwörter, Eigenschaften von e-Mail-Nachrichten (beispielsweise gesendete und empfangene Datumsangaben) oder Dokumenteigenschaften angeben (beispielsweise Dateinamen oder das Datum, an dem ein Dokument zuletzt geändert wurde). Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**. Sie können auch nach vertraulichen Informationen (beispielsweise Sozialversicherungsnummern) in Dokumenten in SharePoint und OneDrive (nicht in e-Mail-Nachrichten) suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Feld **Schlüsselwörter** leer lassen, sind alle Inhalte, die sich an den angegebenen Inhaltsspeicherorten befinden, in den Suchergebnissen enthalten.
    
Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Stichwort oder einen Stichwort Satz eingeben. Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch einen logischen Operator (dargestellt als *c:s*) verbunden, der in der Funktionalität des **or** -Operators in der erstellten Suchabfrage ähnelt. Dies bedeutet, dass Elemente, die ein beliebiges Schlüsselwort in einer beliebigen Zeile enthalten, in den Suchergebnissen enthalten sind.

![Verwenden der Stichwortliste zum Abrufen von Statistiken zu jedem Stichwort in der Abfrage](../media/KeywordListSearch.png)

Gründe für die Verwendung der Stichwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente in der Stichwortliste mit jedem Stichwort übereinstimmen. Dies kann Ihnen helfen, schnell die Schlüsselwörter zu identifizieren, die am häufigsten (und am wenigsten) effektiv sind. Sie können auch eine Stichwort Phrase (umgeben von Klammern) in einer Zeile in der Liste Stichwörter verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistiken](search-statistics.md).

> [!NOTE]
> Um Probleme aufgrund großer Stichwortlisten zu verringern, sind Sie auf maximal 20 Zeilen in der Stichwortliste limitiert.

## <a name="conditions"></a>Bedingungen
    
Sie können Suchbedingungen hinzufügen, um den Umfang einer Suche einzuschränken und eine verfeinerte Ergebnismenge zurückzugeben. Jede Bedingung fügt der Suchabfrage, die erstellt und ausgeführt wird, eine Klausel hinzu, wenn Sie die Suche starten. Eine Bedingung ist logisch mit der Stichwortabfrage (im Feld Schlüsselwort angegeben) durch einen logischen Operator (der als *c:c*dargestellt wird) verbunden, der in der Funktionalität des **and-** Operators ähnelt. Das bedeutet, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in den Suchergebnissen enthalten sein sollen. Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen. Eine Liste und eine Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" unter [Stichwortabfragen und Suchbedingungen](../keyword-queries-and-search-conditions.md#search-conditions).
