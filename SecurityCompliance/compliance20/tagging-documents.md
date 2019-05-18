---
title: Markieren von Dokumenten in einem Prüfdateisatz
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
ms.openlocfilehash: a3b588f4b8e24783cd0d7198ea995f0fd6c8ae3e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154027"
---
# <a name="tag-documents-in-a-review-set"></a>Markieren von Dokumenten in einem Prüfdateisatz

Das Organisieren von Inhalten in einem Überprüfungs Satzes ist wichtig, um verschiedene Workflows im eDiscovery-Prozess abzuschließen. Dies umfasst Folgendes:

-  Ausmerzen unnötiger Inhalte

- Identifizieren relevanter Inhalte
 
-  Identifizieren von Inhalten, die von einem Experten oder einem Anwalt überprüft werden müssen

Wenn Experten, Anwälte oder andere Benutzer Inhalte in einem Überprüfungs Satzes überprüfen, können Ihre Meinungen im Zusammenhang mit den Inhalten mithilfe von Tags erfasst werden. Wenn beispielsweise unnötige Inhalte ausgemerzt werden sollen, kann ein Benutzer Dokumente mit einem Tag wie "nicht reagierende" markieren. Nachdem der Inhalt überprüft und markiert wurde, kann eine Überprüfungs Sätze-Suche erstellt werden, um alle Inhalte auszuschließen, die als "nicht ansprechbar" gekennzeichnet sind, wodurch dieser Inhalt nicht aus den nächsten Schritten im eDiscovery-Workflow entfernt wird. Der Tag-Bereich kann für jeden Fall angepasst werden, sodass die Tags den beabsichtigten Überprüfungsworkflow unterstützen können.

## <a name="tag-types"></a>Tag-Typen

Advanced eDiscovery bietet zwei Typen von Tags:

- **Einzelne Tags** – schränkt Benutzer ein, um ein einzelnes Tag in einer Gruppe auszuwählen. Dies kann hilfreich sein, um sicherzustellen, dass Benutzer nicht in Konflikt stehende Tags wie "reagieren" und "nicht reagierende" auswählen. 

- **Mehrfachauswahl-Tags** – Benutzer können mehrere Tags in einer Gruppe auswählen.

## <a name="tag-structure"></a>Tag-Struktur

Zusätzlich zu den Tag-Typen kann die Struktur der Organisation von Tags im Tag-Panel verwendet werden, um das Markieren von Dokumenten intuitiver zu gestalten. Tags werden nach Abschnitten gruppiert. überprüfen die Option "Suche festlegen" unterstützt die Suche nach Tag und Tag. Dies bedeutet, dass Sie eine Überprüfungs Sätze-Suche erstellen können, um Dokumente mit einem beliebigen Tag in einem Abschnitt abzurufen.

![Markieren von Abschnitten im Tag-Panel](../media/Tagtypes.png)

Tags können weiter organisiert werden, indem Sie in einem Abschnitt verschachtelt werden. Wenn beispielsweise privilegierte Inhalte identifiziert und markiert werden sollen, kann durch Verschachtelung deutlich gemacht werden, dass ein Benutzer ein Dokument als "privilegiert" markieren und den gewünschten Berechtigungstyp auswählen kann, indem das entsprechende geschachtelte Tag überprüft wird.

![Geschachtelte Tags innerhalb eines Tag-Abschnitts](../media/Nestingtags.png)

## <a name="applying-tags"></a>Anwenden von Tags

Es gibt verschiedene Möglichkeiten, ein Tag auf Inhalte anzuwenden.

### <a name="tagging-a-single-document"></a>Markieren eines einzelnen Dokuments

Wenn Sie ein Dokument in einem Überprüfungs Satzes anzeigen, können Sie die Tags anzeigen, die eine Überprüfung verwenden kann, indem Sie auf **Codierungs Bereich**klicken.

![Klicken Sie auf Tag Panel, um das Tag-Panel anzuzeigen](../media/Singledoctag.png)

Auf diese Weise können Sie Tags auf das Dokument anwenden, das im Viewer angezeigt wird.

### <a name="bulk-tagging"></a>Massen Markierung

Das Massen-Tagging kann durch Auswählen mehrerer Dateien im Ergebnisraster und dann mithilfe der Tags im **Codierungs Bereich** wie das Markieren einzelner Dokumente erfolgen. Das Massen-UN-Tagging kann durch zweimaliges Markieren von Tags erfolgen. mit dem ersten Klick wird das Tag angewendet, und die zweite Auswahl stellt sicher, dass das Tag für alle ausgewählten Dateien gelöscht wird.

![Ein Screenshot einer Handy Beschreibung, die automatisch generiert wird](../media/Bulktag.png)

> [!NOTE]
> Bei der Massen Markierung wird im Markierungsbereich die Anzahl der Dateien angezeigt, die für jedes Tag im Bereich markiert sind.

### <a name="tagging-in-other-review-panels"></a>Tagging in anderen Überprüfungs Bereichen

Bei der Überprüfung von Dokumenten können Sie die anderen Überprüfungs Bereiche verwenden, um andere Merkmale von Dokumenten im Ergebnisraster zu überprüfen. Dies umfasst das Überprüfen anderer verwandter Dokumente, e-Mail-Threads, nahe Duplikate und Hash Duplikate. Wenn Sie beispielsweise Verwandte Dokumente überprüfen (mithilfe des Bereichs " **Dokument Familien** Überprüfung"), können Sie die Überprüfungszeit erheblich verringern, indem Sie zugehörige Dokumente in Massen markieren. Wenn beispielsweise eine e-Mail-Nachricht mehrere Anlagen enthält und Sie sicherstellen möchten, dass die gesamte Familie einheitlich markiert ist.

Hier erfahren Sie, wie Sie den Codierungs **Bereich** anzeigen, wenn Sie den **Dokument Familien** -Überprüfungsbereich verwenden:

1. Wenn der Überprüfungsbereich für ein ausgewähltes Dokument geöffnet ist (beispielsweise wird die Liste der verwandten Inhalte im **Dokument Familien** Überprüfungsbereich angezeigt wird, klicken Sie oben im Bereich aktuelle Überprüfung auf **Code Dokumente** .

   Das Dialogfeld Codierung wird angezeigt, das ein Popupfenster ist.

2. Wählen Sie ein oder mehrere Tags aus, um das ausgewählte Dokument anzuwenden. 

3. Zum Markieren aller Dokumente wählen Sie im Bedienfeld " **Dokument Familie** " alle Dokumente aus, klicken Sie auf **Code Dokumente**, und wählen Sie dann die Tags aus, die auf die gesamte Dokumenten Familie angewendet werden sollen.

![Screenshot einer sozialen Medien Bereitstellungs Beschreibung, die automatisch generiert wird](../media/Relatedtag.png)
