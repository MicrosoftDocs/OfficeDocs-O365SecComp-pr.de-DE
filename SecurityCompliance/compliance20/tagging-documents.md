---
title: Markieren von Dokumenten in einem Arbeitssatz
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
ms.openlocfilehash: 510a10386ea51c0397408450f9fc700e9ce6db9c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241116"
---
# <a name="tag-documents-in-a-working-set"></a>Markieren von Dokumenten in einem Arbeitssatz

Das Organisieren von Inhalten in einem Arbeitssatz ist wichtig, um verschiedene Workflows im eDiscovery-Prozess abzuschließen. Dies umfasst Folgendes:

-  AusMerzen unnötiger Inhalte

- Identifizieren relevanter Inhalte
 
-  Identifizieren von Inhalten, die von einem Experten oder Rechtsanwalt überprüft werden müssen

Wenn Experten, Anwälte oder andere Benutzer Inhalte in einem Workingset überarbeiten, können Ihre Meinungen im Zusammenhang mit dem Inhalt mithilfe von Tags erfasst werden. Wenn beispielsweise unnötige Inhalte abgeschlachtet werden sollen, kann ein Benutzer Dokumente mit einem Tag wie "nicht reagieren" markieren. Nachdem der Inhalt überprüft und markiert wurde, kann eine Working Set-Suche erstellt werden, um Inhalte zu ausschließen, die als "nicht reaktionsfähig" gekennzeichnet sind, wodurch dieser Inhalt nicht aus den nächsten Schritten im eDiscovery-Workflow entfernt wird. Das Tag-Panel kann für jeden Fall angepasst werden, sodass die Tags den beabsichtigten Übersichts Workflow unterstützen können.

## <a name="tag-types"></a>Tag-Typen

Advanced eDiscovery (Preview) bietet zwei Arten von Tags:

- **Single Choice Tags** -schränkt die Benutzer ein, um ein einzelnes Tag innerhalb einer Gruppe auszuwählen. Dies kann nützlich sein, um sicherzustellen, dass Benutzer keine Konflikt verursachenden Tags wie "reaktionsschnelle" und "nicht reagierende" auswählen. 

- **Multiple Choice Tags** – ermöglicht Benutzern das Auswählen mehrerer Tags innerhalb einer Gruppe.

## <a name="tag-structure"></a>Tag-Struktur

Zusätzlich zu den Tag-Typen kann die Struktur der Organisation von Tags im Tag-Panel verwendet werden, um die intuitive Kennzeichnung von Dokumenten zu vereinfachen. Tags werden nach Abschnitten gruppiert. Working Set Search unterstützt die Möglichkeit, nach Tag und nach Tag zu suchen. Dies führt dazu, dass Sie eine Working Set-Suche erstellen können, um Dokumente abzurufen, die mit einem beliebigen Tag in einem Abschnitt getaggt sind.

![Tag-Abschnitte im Beschriftungsbereich](../media/Tagtypes.png)

Tags können weiter organisiert werden, indem Sie innerhalb eines Abschnitts geschachtelt werden. Wenn die Absicht beispielsweise darin besteht, privilegierte Inhalte zu identifizieren und zu markieren, kann Verschachtelung verwendet werden, um deutlich zu machen, dass ein Benutzer ein Dokument als privilegiert markieren und den Typ der Rechte auswählen kann, indem Sie das entsprechende geschachtelte Tag überprüfen.

![Geschachtelte Tags innerhalb eines Tag-Abschnitts](../media/Nestingtags.png)

## <a name="applying-tags"></a>Anwenden von Tags

Es gibt mehrere Möglichkeiten, ein Tag auf Inhalte anzuwenden.

### <a name="tagging-a-single-document"></a>Markieren eines einzelnen Dokuments

Wenn Sie ein Dokument in einem Arbeitssatz anzeigen, können Sie die von einer Überprüfungen verwendeten Tags anzeigen, indem Sie auf **Codebereich**klicken.

![Klicken Sie auf das Beschriftungsfeld, um den Beschriftungsbereich anzuzeigen.](../media/Singledoctag.png)

Auf diese Weise können Sie Tags auf das im Viewer angezeigte Dokument anwenden.

### <a name="bulk-tagging"></a>Massen Kennzeichnung

Massen Kennzeichnungen können vorgenommen werden, indem mehrere Dateien im Ergebnisraster ausgewählt werden und die Tags im Codierungs **Bereich** ähnlich wie beim taggen einzelner Dokumente verwendet werden. Bulk-UN-Tagging kann durch die Auswahl von Tags zweimal durchgeführt werden; mit dem ersten Klick wird das-Tag angewendet, und bei der zweiten Auswahl wird sichergestellt, dass das Tag für alle ausgewählten Dateien deaktiviert ist.

![Screenshot einer automatisch generierten Mobiltelefon Beschreibung](../media/Bulktag.png)

> [!NOTE]
> Beim Massen Tagging zeigt das Markierungsfeld die Anzahl der Dateien an, die für jedes Tag im Bereich markiert sind.

### <a name="tagging-in-other-review-panels"></a>Tagging in anderen Überprüfungen

Beim Überprüfen von Dokumenten können Sie die anderen Überprüfungs Bereiche verwenden, um andere Merkmale von Dokumenten im Ergebnisraster zu überprüfen. Hierzu gehören die Überprüfung anderer verwandter Dokumente, e-Mail-Threads, in der Nähe von Duplikaten und Hash Duplikate. Beispielsweise können Sie bei der Überprüfung zugehöriger Dokumente (über den Bereich " **Dokument Familien** Überprüfung") die Überprüfungszeit erheblich reduzieren, indem Sie verwandte Dokumente mit einem Massen Kennzeichnungsvorgang versehen. Wenn eine e-Mail-Nachricht beispielsweise mehrere Anlagen enthält und Sie sicherstellen möchten, dass die gesamte Familie konsistent gekennzeichnet wird.

Hier erfahren Sie beispielsweise, wie Sie das **Codierungspanel** bei Verwendung des **Dokument Familien** Übersichtsfensters anzeigen:

1. Wenn das Überarbeitungsfenster für ein ausgewähltes Dokument geöffnet wird (beispielsweise Anzeigen der Liste mit verwandten Inhalten im Bereich **Dokument Familien** Überprüfung), klicken Sie oben im aktuellen überarbeitungsFenster auf **Code Dokumente** .

   Der Codierungs Bereich wird als Popupfenster angezeigt.

2. Wählen Sie ein oder mehrere Tags aus, um das ausgewählte Dokument zu übernehmen. 

3. Um alle Dokumente zu markieren, wählen Sie im Bedienfeld der **Dokument Familie** alle Dokumente aus, klicken Sie auf **Code Dokumente**, und wählen Sie dann die Tags aus, die auf die gesamte Dokumenten Familie angewendet werden sollen.

![Ein Screenshot einer Beschreibung des sozialen Medien Beitrags wird automatisch generiert.](../media/Relatedtag.png)
