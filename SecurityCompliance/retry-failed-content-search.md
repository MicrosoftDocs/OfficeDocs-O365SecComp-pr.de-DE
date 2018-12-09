---
title: Wiederholen Sie eine Suche Inhalt, um einen Inhaltsspeicherort Fehler zu beheben
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Verwenden Sie die Schaltfläche "Wiederholen" für Resolve Inhalte durchsucht, die Inhaltsspeicherort Fehler enthalten.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210186"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a>Wiederholen Sie eine Suche Inhalt, um einen Inhaltsspeicherort Fehler zu beheben

Wenn Sie eine große Anzahl von Postfächern (z. B. Suche 100.000 Postfächer oder mehrere in einer einzelnen Inhaltssuche) suchen Inhaltssuche in die Office 365-Sicherheit und Compliance Center verwenden, erhalten Sie möglicherweise Search-Fehler, die den folgenden ähneln:

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

Diese Fehler (mit Fehlercodes CS008-009 und CS012-002) anzugeben, dass Inhalte Suche beim Durchsuchen der Speicherorte für bestimmte Inhalte Fehler; In diesem Beispiel wurden nicht zwei Postfächer durchsucht. Diese Fehler werden auf der Seite Status Details flyoutmenü, der die Inhaltssuche angezeigt.

## <a name="cause-of-content-location-errors"></a>Ursache für Fehler Content-location

Wenn Sie eine große Anzahl von Postfächern zu suchen, wird die Suche auf Tausende von Servern in einem Microsoft-Datencenter verteilt. Eine jederzeit konnte bestimmte Server im Zustand Neustart oder beim Ausführen eines Failovers für redundante Kopien sein. In beiden Fällen wird die Inhaltssuche-Anforderung zum Abrufen von Daten Timeout. Im vorherigen Beispiel wurden die Fehler für die Postfächer, die nicht das Ergebnis der Suche Timeout.

## <a name="resolving-content-location-errors"></a>Auflösen von Fehlern Content-location

Neustarten der Suche führt häufig zu ähnliche Fehler auf unterschiedlichen Servern. Anstatt einen Neustart für die Suche aus, klicken Sie auf die Schaltfläche **Wiederholen** , die am oberen Rand der Seite mit den Suchergebnissen angezeigt wird.

![Klicken Sie auf die Schaltfläche "Wiederholen", um Inhaltsspeicherort Fehler zu beheben](media/retrycontentsearch3.png)

Dadurch wird die Suche nur für die Postfächer, die nicht wiederholen. Wenn Sie die Suche wiederholen, bleiben die anderen Ergebnisse, die erfolgreich zurückgegeben wurden.

## <a name="tips-to-avoid-content-location-errors"></a>Tipps zur Vermeidung von Inhaltsspeicherort Fehler

Hier sind einige Fehlerursachen Inhaltsspeicherort hinzufügen und einige Tipps zur einfacheren vermeiden, große Anzahl von Postfächern zu suchen.

- Das Postfach, das durchsucht wird möglicherweise aufgrund Benutzeraktivität ausgelastet. In diesem Fall möglicherweise selbst, um zu verhindern, dass das Postfach zu einem Ausfall des Suchdiensts drosseln. Um dies zu vermeiden, führen Sie Suchvorgänge während der Geschäftszeiten.

- Die Suchabfrage möglicherweise zu viel Inhalt aus dem Postfach abgerufen werden. Wenn möglich, versuchen Sie, die Suche mithilfe von Schlüsselwörtern, Datumsbereiche und Suchkriterien einzugrenzen.

- Zu viele Schlüsselwörter oder Schlüsselwort Ausdrücke beim Erstellen einer Suchabfrage mithilfe der [Liste der Schlüsselwörter](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Beim Ausführen einer Suchabfrage, die der Liste Schlüsselwörter verwendet, führt der Dienst im Wesentlichen eine separate Suche für jede Zeile in der Schlüsselwortliste, sodass Statistiken generiert werden können. Wenn Sie die Liste der Schlüsselwörter in Suchabfragen verwenden, minimieren Sie die Anzahl der Zeilen in der Schlüsselwortliste oder Teilen Sie die Zahl Schlüsselwörter in kleinere Listen, und erstellen Sie eine andere Suche für jede Schlüsselwortliste.

  > [!NOTE]
  > Zur Verringerung der Probleme aufgrund von großen Listen Sie nun auf ein Maximum von 20 Zeilen in der Schlüsselwortliste einer Suchabfrage begrenzt.

- Zu viele Suchvorgänge werden mit demselben Postfach zur selben Zeit ausgeführt wird. Versuchen Sie wenn möglich, eine Suche auf eine beliebige ein Postfach zu einem Zeitpunkt auszuführen.

- Suchen in einem einzelnen Suchvorgang zu viele Postfächer. Die Wahrscheinlichkeit der Inhaltsspeicherort Fehler erhöht, wenn eine große Anzahl von Postfächern zu suchen. Versuchen Sie nach Möglichkeit, mehrere Suchvorgänge durchgeführt werden, damit jeder Suche eine Teilmenge der Postfächer in Ihrer Organisation enthält.

- Erforderliche Wartung wird für das Postfach durchgeführt. Obwohl diese Ursache wahrscheinlich selten auftritt, warten Sie einen Moment während nach dem Empfang des Inhaltsspeicherort Fehlers, und wiederholen Sie die Suche.
