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
description: ''
ms.openlocfilehash: a33ecb6e1a2549b6bdc3bde9897b8a75e742b482
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151927"
---
# <a name="build-search-queries"></a>Erstellen von Suchabfragen

Bei der Erstellung Ihrer Abfrage können Sie verschiedene Schlüsselwörter und Bedingungen verwenden, um zu definieren, welche Elemente gesucht werden sollen.

## <a name="keyword-searches"></a>Stichwortsuche

Geben Sie im Feld **Schlüsselwörter** eine Suchabfrage ein. Sie können Schlüsselwörter, Nachrichteneigenschaften , z. B. Sende- und Empfangsdatum, oder Dokumenteigenschaften angeben, z. B. Dateinamen oder das Datum der letzten Dokumentänderung. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**. Sie können auch nach vertraulichen Informationen (wie etwa Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Feld Schlüsselwort leer lassen, werden alle Inhalte, die sich an den angegebenen Inhaltsspeicherorten befinden, in die Suchergebnisse eingeschlossen.
    
Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** und in jede Zeile ein Schlüsselwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter für jede Zeile durch einen logischen Operator ( **c:s**) verbunden, der in der Funktionalität des **or** -Operators in der erstellten Suchabfrage ähnelt. 
    
Gründe für die Verwendung der Stichwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit den einzelnen Schlüsselwörtern übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Stichwörter am häufigsten (und am wenigsten) effektiv sind. Sie können auch eine Stichwort Phrase (umgeben von Klammern) in einer Zeile verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistik](search-statistics.md).

## <a name="conditions"></a>Bedingungen
    
Sie können Suchbedingungen hinzufügen, um eine Suche einzuschränken und eine verfeinerte Ergebnismenge zurückzugeben. Jede Bedingung fügt der Suchabfrage, die erstellt und ausgeführt wird, eine Klausel hinzu, wenn Sie die Suche starten. Eine Bedingung ist logisch mit der Stichwortabfrage (im Feld Schlüsselwort angegeben) durch einen logischen Operator (**c:c**) verbunden, der in der Funktionalität des **and-** Operators ähnelt. Das bedeutet, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in den Ergebnissen enthalten sein sollen. Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen. Eine Liste und eine Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](../keyword-queries-and-search-conditions.md#search-conditions).


