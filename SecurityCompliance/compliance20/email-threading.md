---
title: E-Mail-Threading
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
ms.openlocfilehash: a3c4f940c34a9c51bf58107d10e04d0ed60f28a8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213425"
---
# <a name="email-threading"></a>E-Mail-Threading

Betrachten Sie eine e-Mail-Unterhaltung, die schon eine Weile geht. In den meisten Fällen enthält die letzte e-Mail des Threads den Inhalt aller vorhergehenden e-Mails. durch das Überprüfen der letzten e-Mail erhalten Sie einen vollständigen Kontext der Unterhaltung im Thread. E-Mail-Threading identifiziert solche e-Mails, sodass Prüfer einen Bruchteil der gesammelten Dokumente überarbeiten können, ohne dass ein Kontext verloren geht.

## <a name="what-does-email-threading-do"></a>Was bewirkt die e-Mail-Threading?

E-Mail-Threading analysiert jede e-Mail und desconstructs Sie an einzelne Nachrichten. jede e-Mail ist eine Kette von einzelnen Nachrichten. Dann analysiert sie alle e-Mails im Arbeitssatz, um zu bestimmen, ob eine e-Mail eindeutige Inhalte enthält oder ob die Kette vollständig in einer anderen e-Mail enthalten ist. Am Ende werden e-Mails in vier Kategorien unterteilt:

- **Inclusive**: die letzte Nachricht in der e-Mail hat eindeutige Inhalte, und die e-Mail verfügt über alle Anhänge, die in anderen e-Mails enthalten waren, von denen der Inhalt vollständig in dieser e-Mail enthalten ist.


- **Inklusive minus**: die letzte Nachricht in der e-Mail hat eindeutige Inhalte, aber die e-Mail enthält nicht einige der Anhänge, die in anderen e-Mails enthalten waren, von denen der Inhalt vollständig in dieser e-Mail enthalten ist.

- **Inklusive Kopie**: eine exakte Kopie einer inklusive/inklusive minus-e-Mail

- **None**: der Inhalt dieser e-Mail ist vollständig in mindestens einer e-Mail enthalten, die als inclusive/inklusive minus gekennzeichnet ist.

## <a name="how-is-it-different-from-conversations-in-outlook"></a>Wie unterscheidet sich das von Outlook?
Auf einen Blick klingt dies sehr ähnlich wie Konversations Gruppierungen in Outlook. Es gibt jedoch einige wichtige Unterschiede. Betrachten Sie eine e-Mail-Unterhaltung, die in zwei Unterhaltungen verzweigt wurde; Beispielsweise hat jemand auf eine e-Mail geantwortet, die nicht die neueste in der Unterhaltung ist, sodass die letzten beiden e-Mails in der Unterhaltung einen eindeutigen Inhalt aufweisen.

Outlook würde die e-Mails weiterhin in einer einzigen Unterhaltung gruppieren; das Lesen der letzten e-Mail würde bedeuten, dass der Kontext der letzten e-Mail, die auch eindeutigen Inhalt enthält, fehlt. Da e-Mail-Threading jede e-Mail in einzelne Komponenten auswertet und vergleicht, würde das e-Mail-Threading beide der letzten beiden e-Mails als inclusive markieren, um sicherzustellen, dass Sie keinen Kontext verpassen, solange Sie alle als inclusive markierten e-Mails lesen.