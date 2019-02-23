---
title: Analysieren von Daten in einem Arbeitssatz in Advanced eDiscovery (Preview)
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
ms.openlocfilehash: ae024f423ac9b4ab9210ddfab519093a9fee3e42
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216795"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a>Analysieren von Daten in einem Arbeitssatz in Advanced eDiscovery (Preview)

Wenn die Anzahl der gesammelten Dokumente groß ist, kann es schwierig sein, Sie alle zu überarbeiten. Advanced eDiscovery (Preview) bietet eine Reihe von Tools, mit denen die Dokumente analysiert werden können, um den Umfang der zu überprüfenden Dokumente ohne Verlust an Informationen zu reduzieren und Sie bei der Organisation der Dokumente auf kohärente Weise zu unterstützen. Weitere Informationen zu diesen Funktionen finden Sie unter:

- [Erkennen von Quasiduplikaten](near-duplicates.md)
- [E-Mail-Threading](email-threading.md)
- [Designs](themes.md)

So analysieren Sie Daten in einem Arbeitssatz:

1. Konfigurieren Sie Analyse Einstellungen für Ihren Fall. Weitere Informationen finden Sie unter [Configure Search and Analytics Settings](configure-search-analytics-settings.md).
2. Öffnen Sie den zu analysierenden Arbeitssatz.
3. Wechseln Sie zu "Arbeitsmappe verwalten".
4. Klicken Sie auf "analysieren".

Sie können den Fortschritt der Analyse auf der Registerkarte Aufträge in Ihrem Fall überprüfen.

 Nach Abschluss der Analyse können Sie Analyseberichte anzeigen, Abfragen in Ihrem Workingset für die Ergebnisse der Analyse ausführen (Weitere Informationen finden Sie unter [Abfrage innerhalb des Arbeitssatzes](working-set-search.md)) und weitere Informationen zu einem bestimmten Dokument anzeigen (mehr dazu finden Sie unter [ ÜberPrüfen von Daten im Arbeitssatz](reviewing-data-in-working-set.md)).

## <a name="analytics-report"></a>Analysebericht

So zeigen Sie einen Analysebericht für Ihren Arbeitssatz an

1. Öffnen Sie Ihre Arbeitsmappe.
2. Wechseln Sie zu "Arbeitsmappe verwalten".
3. Klicken Sie auf "Bericht".

Der Bericht enthält vier Komponenten aus der Analyse:

- **Aufteilung** -wie viele e-Mails, Anlagen und lose Dokumente im Arbeitssatz gefunden wurden.

- **Dokumente (ausgenommen Anlagen)** -wie viele Lose Dokumente waren Pivots, eindeutige nahe Duplikate eines Pivots oder ein genaues Duplikat eines anderen Dokuments.

- **E-Mails** -wie viele e-Mails inklusive, einschließlich Kopien, inklusive minus, oder keines der obigen.

- **Attachments** -wie viele e-Mail-Anlagen waren eindeutig oder Duplikate einer anderen e-Mail-Anlage innerhalb des Arbeitssatzes.