---
title: Analysieren von Daten in einem Übersichts Satz in Advanced eDiscovery
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
description: ''
ms.openlocfilehash: c765234e1aa0738415f66f90b66ebce0fcab2505
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527171"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a>Analysieren von Daten in einem Übersichts Satz in Advanced eDiscovery

Wenn die Anzahl der gesammelten Dokumente groß ist, kann es schwierig sein, Sie alle zu überarbeiten. Advanced eDiscovery bietet eine Reihe von Tools, mit denen Sie die Dokumente analysieren können, um den Umfang der zu überprüfenden Dokumente ohne Verlust von Informationen zu reduzieren und Sie bei der Organisation der Dokumente auf kohärente Weise zu unterstützen. Weitere Informationen zu diesen Funktionen finden Sie unter:

- [Erkennen von Quasiduplikaten](near-duplicates.md)

- [E-Mail-Threading](email-threading.md)

- [Designs](themes.md)

So analysieren Sie Daten in einem Übersichts Satz:

1. Konfigurieren Sie Analyse Einstellungen für Ihren Fall. Weitere Informationen finden Sie unter [Configure Search and Analytics Settings](configure-search-analytics-settings.md).

2. Öffnen Sie den Übersichts Satz, den Sie analysieren möchten.

3. Klicken Sie auf Übersichts **Satz verwalten**.

4. Klicken Sie auf **analysieren**.

Sie können den Fortschritt der Analyse auf der Registerkarte **Aufträge** des Falls überprüfen.

 Nach Abschluss der Analyse können Sie Analyseberichte anzeigen, Abfragen in Ihrem Überprüfungs Satz für die Ergebnisse der Analyse ausführen (siehe [Abfrage innerhalb](review-set-search.md)des Überprüfungs Satzes) und verwandte Dokumente eines bestimmten Dokuments anzeigen (siehe Überprüfen von [Daten im](reviewing-data-in-review-set.md)Überprüfungs Satz).

## <a name="analytics-report"></a>Analysebericht

So zeigen Sie einen Analysebericht für einen Übersichts Satz an:

1. Öffnen Sie den Übersichts Satz.

2. Klicken Sie auf Übersichts **Satz verwalten**.

3. Klicken Sie auf **Bericht**.

Der Bericht enthält vier Komponenten aus der Analyse:

- **Aufteilung** -wie viele e-Mail-Nachrichten, Anlagen und lose Dokumente wurden im Übersichts Satz gefunden.

- **Dokumente (ausgenommen Anlagen)** -wie viele Lose Dokumente waren Pivots, eindeutige nahe Duplikate eines Pivots oder ein genaues Duplikat eines anderen Dokuments.

- **E-Mails** -wie viele e-Mail-Nachrichten inklusive, einschließlich Kopien, inklusive minus, oder keines der obigen.

- **Attachments** -wie viele e-Mail-Anlagen waren eindeutig oder Duplikate einer anderen e-Mail-Anlage im Übersichts Satz.