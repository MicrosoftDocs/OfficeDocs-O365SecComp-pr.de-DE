---
title: Einblick für langsame Nachrichtenflussregeln
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 5/3/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: Administratoren erfahren mehr über die langsamen Nachrichtenfluss Regeln im Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center.
ms.openlocfilehash: e1ce23c94cd5260d8a7a7ebd99521a4a6f5c7b0a
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30720255"
---
# <a name="slow-mail-flow-rules-insight"></a>Einblick für langsame Nachrichtenflussregeln

Ineffiziente Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) können zu Verzögerungen bei der Nachrichtenübermittlung für Ihre Organisation führen. Dieser Einblick meldet Nachrichtenfluss Regeln, die sich auf den Nachrichtenfluss Ihrer Organisation auswirken. Beispiele für diese Regeln sind:

- Bedingungen, die für umfangreiche Gruppen **Mitglied sind** .

- Bedingungen, die einen komplexen regulären Ausdruck (Regex)-Mustervergleich verwenden.

- Bedingungen, die die Inhaltsüberprüfung in Anlagen verwenden.

Die Einblicke helfen Ihnen bei der Identifizierung und Optimierung von Nachrichtenfluss Regeln, um die Verzögerungen bei der Nachrichtenübermittlung zu verringern.

![Eine langsame Nachrichtenfluss Regel Einblicke in das Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

Wenn Sie auf **Details anzeigen**klicken, wird ein Flyout-Bereich angezeigt, in dem Sie die Regel überprüfen können. Klicken Sie im Flyoutbereich auch auf **Beispiel Nachrichten anzeigen** , um zu sehen, welche Art von Nachrichten von der Regel betroffen sind.

![Flyout-Bereich nach dem Klicken auf Details anzeigen in einem langsamen Nachrichtenfluss Regeln Einblicke in das Nachrichtenfluss-Dashboard](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)

## <a name="see-also"></a>Siehe auch

Weitere Informationen zu anderen Nachrichtenfluss Einblicken im Nachrichtenfluss-Dashboard finden Sie unter [Nachrichtenfluss Einblicke im Security _AMP_ Compliance Center](mail-flow-insights.md).
