---
title: Führen Sie Analysen aus, um schneller zu untersuchen
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
ms.openlocfilehash: 9516035fb6c758fdff1852249fff2815f19af559
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030119"
---
# <a name="run-analytics-to-investigate-faster"></a>Führen Sie Analysen aus, um schneller zu untersuchen

Wenn eine Beweissammlung groß ist, kann es schwierig sein, Sie alle zu überarbeiten. Ein Satz von nachweisen umfasst häufig mehrere Kopien derselben oder ähnlicher e-Mail-Nachrichten oder Dokumente. Data Investigations (Preview) bietet eine Reihe von Analysetools, mit denen Sie den Umfang der zu überprüfenden Dokumente ohne Verlust an Informationen reduzieren können. Weitere Informationen zu diesen Funktionen finden Sie unter:

- [Erkennen von Quasiduplikaten](near-duplicates.md)

- [E-Mail-Threading](email-threading.md)

- [Designs](themes.md)

So analysieren Sie Daten in einem Beweissatz:

1. Konfigurieren Sie die Analyse Einstellungen für Ihre Untersuchung. Weitere Informationen finden Sie unter [Configure Search and Analytics Settings](configure-search-analytics-settings.md).

2. Öffnen Sie den Evidence-Satz.

3. Klicken Sie auf **Evidence verwalten**.

4. Klicken Sie unter **Analyse**auf **analysieren**.

Sie können den Fortschritt der Analyse auf der Registerkarte **Aufträge** in der Untersuchung überprüfen. Der ausgelöste Auftragstyp heißt **Running Analytics**.

 Nach Abschluss der Analyse kann eine Liste der exakten Duplikate oder nahezu Duplikate des Dokuments angezeigt werden, das Sie im Bereich auf der rechten Seite überprüfen. Um alle Duplikate des Dokuments auszuwählen, das Sie anzeigen, können Sie dieses Panel ganz einfach verwenden. Weitere Informationen zu anderen Features in diesem Bereich finden Sie unter [Überprüfen von Daten in Evidence](review-data-in-evidence.md). 

Sie können auch zusätzliche Abfragen innerhalb ihres Beweises ausführen, indem Sie die Ergebnisse der Analyse wie Designs verwenden. Weitere Informationen finden Sie unter [Abfragen der Daten in Evidence](evidence-query.md).

## <a name="analytics-report"></a>Analysebericht

So zeigen Sie einen Analysebericht für Ihren Nachweis an:

1. Öffnen Sie den Evidence-Satz.

2. Klicken Sie auf **Evidence verwalten**.

3. Klicken Sie unter **Analytics**auf **Bericht anzeigen**.

Der Bericht enthält vier Komponenten aus der Analyse:

- **Breakdown** – die Anzahl der RAW-e-Mails, Anlagen und Dokumente, die im Beweissatz enthalten sind.

- **E-Mails** -die Anzahl der eamil-Nachrichten, die inklusive minus-, inklusive-Kopien oder keiner der oben genannten enthalten sind.
   - Inklusivs: die letzte Nachricht im e-Mail-Thread, die alle Vorgeschichte enthält und Überprüfungen erfordert.
   - Inklusive minus: die Nachricht im Thread, die mindestens eine Anlage enthält, die überprüft werden muss.
   - Inklusive Kopien: die Nachricht, die eine Kopie einer anderen inklusiven oder inklusiven minus Nachricht (Betreff und Text) ist.

- **Attachments** – die Anzahl von e-Mail-Anlagen, die eindeutig sind, oder Duplikate einer anderen e-Mail-Anlage innerhalb desselben Beweismaterials.

- **Dokumente (ausgenommen e-Mail-Anhänge)** – die Anzahl der eindeutigen Dokumente, die überprüft werden müssen, beispielsweise das repräsentativste Dokument der nahezu doppelten Gruppe oder ein genaues Duplikat eines anderen Dokuments).