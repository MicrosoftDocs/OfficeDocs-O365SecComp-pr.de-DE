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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 8e7f3d798d3b6cfe25d57b941ed2be1d8d5e92b6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216985"
---
# <a name="build-search-queries"></a>Erstellen von Suchabfragen

Beim Erstellen einer Abfrage können Sie verschiedene Schlüsselwörter und Bedingungen verwenden, um zu definieren, welche Elemente gesucht werden soll.

## <a name="keyword-searches"></a>Stichwortsuche

Geben Sie im Feld **Stichwörter** eine Suchabfrage ein. Sie können Schlüsselwörter, Nachrichteneigenschaften wie gesendete und empfangene Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, an dem ein Dokument zuletzt geändert wurde, angeben. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**. Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in die Suchergebnisse eingeschlossen.
    
Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Stichwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch einen logischen Operator ( **c:s**) verbunden, der in der Funktionalität mit dem **or** -Operator in der erstellten Suchabfrage vergleichbar ist. 
    
Gründe für die Verwendung der Keyword-Liste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit jedem Stichwort übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Schlüsselwörter am meisten (und am wenigsten) wirksam sind. Sie können auch eine Schlüsselwortphrase (umgeben von Klammern) in einer Zeile verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistik](search-statistics.md).

## <a name="conditions"></a>Bedingungen
    
Sie können Suchbedingungen hinzufügen, um eine Suche einzuschränken und eine genauere Ergebnismenge zurückzugeben. Jede Bedingung fügt eine Klausel zu der Suchabfrage hinzu, die erstellt und beim Starten der Suche ausgeführt wird. Eine Bedingung ist logisch mit der Stichwortabfrage (angegeben im Stichwortfeld) durch einen logischen Operator (**c:c**) verbunden, der in der Funktionalität mit dem **and-** Operator vergleichbar ist. Dies führt dazu, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in die Ergebnisse eingeschlossen werden sollen. Auf diese Weise können Sie Ihre Ergebnisse einschränken. Eine Liste und Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" in [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](../keyword-queries-and-search-conditions.md#search-conditions).


