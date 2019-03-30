---
title: Wiederholen einer Inhaltssuche zum Beheben eines Inhaltsspeicherort Fehlers
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Verwenden Sie die Schaltfläche wiederHolen zum Auflösen von Inhalts suchVorgängen, die Inhaltsspeicherort Fehler aufweisen.
ms.openlocfilehash: 8334ec053e86e48f99955af2d56e511a2df5c25a
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998998"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a>Wiederholen einer Inhaltssuche zum Beheben eines Inhaltsspeicherort Fehlers

Wenn Sie die Inhaltssuche im Security and Compliance Center verwenden, um eine sehr große Anzahl von Postfächern zu durchsuchen (beispielsweisedurch suchen von 100.000 Postfächern oder mehr in einer einzelnen Inhaltssuche), werden möglicherweise Suchfehler angezeigt, die den folgenden ähneln:

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

Diese Fehler (mit Fehlercodes von CS008-009 und CS012-002) deuten darauf hin, dass die Inhaltssuche bestimmte inhaltsspeicherorte nicht durchsuchen konnte. in diesem Beispiel wurden zwei Postfächer nicht durchsucht. Diese Fehler werden auf der Seite mit dem Statusdetails-Flyout der Inhaltssuche angezeigt.

## <a name="cause-of-content-location-errors"></a>Ursache von Inhaltsspeicherort Fehlern

Beim Durchsuchen einer hohen Anzahl von Postfächern wird die Suche über Tausende von Servern in einem Microsoft-Datencenter verteilt. Zu einem beliebigen Zeitpunkt können bestimmte Server im Neustartstatus oder bei einem Failover auf redundante Kopien sein. In beiden Fällen wird die Anforderung der Inhaltssuche zum Abrufen von Daten Timeout. Im vorherigen Beispiel waren die Fehler für die Postfächer, die fehlgeschlagen waren, das Ergebnis des Such Timeouts.

## <a name="resolving-content-location-errors"></a>Auflösen von Inhaltsspeicherort Fehlern

Das Neustarten der Suche führt häufig zu ähnlichen Fehlern auf verschiedenen Servern. Anstatt die Suche neu zu starten, klicken Sie oben auf der Suchergebnisseite auf die Schaltfläche wieder **holen** .

![Klicken Sie auf die Schaltfläche wiederholen, um Fehler bei der Inhalts Lokalisierung zu beheben](media/retrycontentsearch3.png)

Dies führt dazu, dass die Suche nur für die Postfächer erneut versucht wird, bei denen ein Fehler aufgetreten ist. Wenn Sie die Suche wiederholen, werden die anderen Ergebnisse, die erfolgreich zurückgegeben wurden, beibehalten.

## <a name="tips-to-avoid-content-location-errors"></a>Tipps zur Vermeidung von Inhaltsspeicherort Fehlern

Im folgenden finden Sie einige zusätzliche Ursachen für Fehler im Inhaltsspeicherort und einige Tipps, die Ihnen bei der Suche nach einer hohen Anzahl von Postfächern helfen.

- Das zu durchsuchende Postfach ist aufgrund der Benutzeraktivität möglicherweise ausgelastet. In diesem Fall kann der Suchdienst sich selbst Drosseln, um zu verhindern, dass das Postfach nicht mehr verfügbar ist. Um dies zu vermeiden, führen Sie Suchvorgänge außerhalb der Geschäftszeiten aus.

- Die Suchabfrage kann zu viele Inhalte aus dem Postfach abrufen. Versuchen Sie nach Möglichkeit, den Bereich der Suche mithilfe von Stichwörtern, Datumsbereichen und Suchbedingungen einzugrenzen.

- Zu viele Schlüsselwörter oder Stichwort Ausdrücke beim Erstellen einer Suchabfrage mithilfe der [Stichwörter Liste](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Wenn Sie eine Suchabfrage ausführen, die die Stichwörter Liste verwendet, führt der Dienst im Wesentlichen eine separate Suche für jede Zeile in der Schlüsselwortliste aus, damit Statistiken generiert werden können. Wenn Sie die Liste Stichwörter in Suchabfragen verwenden, minimieren Sie die Anzahl der Zeilen in der Keyword-Liste, oder Teilen Sie die Zahlen Schlüsselwörter in kleinere Listen auf, und erstellen Sie eine andere Suche für jede Keyword-Liste.

  > [!NOTE]
  > Um Probleme zu vermeiden, die durch umfangreiche Stichwortlisten verursacht werden, sind Sie jetzt auf maximal 20 Zeilen in der Stichwortliste einer Suchabfrage beschränkt.

- Zu viele Suchvorgänge werden gleichzeitig für dasselbe Postfach durchgeführt. Versuchen Sie nach Möglichkeit, eine Suche gleichzeitig an einem beliebigen Postfach auszuführen.

- Durchsuchen zu vieler Postfächer in einer einzelnen Suche. Bei der Suche nach einer sehr großen Anzahl von Postfächern erhöht sich die Wahrscheinlichkeit von Inhaltsspeicherort Fehlern. Versuchen Sie nach Möglichkeit, mehrere Suchvorgänge auszuführen, damit jede Suche eine Teilmenge der Postfächer in Ihrer Organisation enthält.

- Erforderliche Wartung für das Postfach. Obwohl diese Ursache wahrscheinlich selten auftritt, warten Sie eine Weile nach Erhalt des Inhaltsspeicher Fehlers, und wiederholen Sie die Suche.
