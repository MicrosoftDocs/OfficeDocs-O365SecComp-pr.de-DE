---
title: Threading-e-Mail
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 2340128f508a3be389afce86596f7e6395a0bb7e
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607809"
---
# <a name="email-threading"></a>Threading-e-Mail
Erwägen Sie eine e-Mail-Unterhaltung, die für eine Weile schon hat. In den meisten Fällen muss die letzte e-Mail auf dem Thread den Inhalt aller vorherigen e-Mails enthalten; So überprüfen Sie die letzte e-Mail erhalten einen vollständigen Kontext der Unterhaltung, die im Thread erfolgt. Derartige e-Mails threading-e-Mail identifiziert werden, so dass Bearbeiter einen Bruchteil gesammelten Dokumente überprüfen können, ohne zu einem beliebigen Kontext verlieren.

## <a name="what-does-email-threading-do"></a>Was macht threading-e-Mail?
E-Mail-threading jede e-Mail- und Desconstructs analysiert, um einzelne Nachrichten; Jede e-Mail ist eine Kette von einzelnen Nachrichten. Klicken Sie dann, analysiert alle e-Mails des Arbeitssatzes, um zu bestimmen, ob eine e-Mail-Nachricht eindeutig Inhalt aufweist oder ob die Kette vollständig in eine andere e-Mail-Adresse enthalten ist. Am Ende sind-e-Mails in vier Kategorien unterteilt:
- Inclusives: die letzte Nachricht in der e-Mail eindeutigen Inhalt und die e-Mail-Nachricht hat alle Anlagen, die in anderen e-Mails enthalten waren, von denen die Inhalte vollständig in dieser e-Mail enthalten ist.
- Minus inklusive: die letzte Meldung in der e-Mail hat eindeutige Inhalt, die e-Mail enthält jedoch keine einige der Anlagen, die in anderen e-Mails enthalten waren, von denen die Inhalte vollständig in diese e-Mail enthalten ist.
- Inklusive Kopie: eine genaue Kopie eines inklusive/inklusive minus e-Mail
- None: Der Inhalt dieser e-Mail ist vollständig in mindestens eine e-Mail-Nachricht enthalten, die als inklusive/inklusive Minuszeichen gekennzeichnet ist.

## <a name="how-is-it-different-from-conversations-in-outlook"></a>Wie ist es sich von Unterhaltungen in Outlook?
Auf einen Blick hört Unterhaltung Gruppen in Outlook sehr ähnlich. Es gibt jedoch einige wichtige Unterschiede. Verwenden Sie eine e-Mail-Unterhaltung, die in zwei Unterhaltung verzweigt, haben Sie; beispielsweise geantwortet einer Person an eine e-Mail, die nicht die neuesten in der Unterhaltung ist, sodass die letzten beiden e-Mails in der Unterhaltung sowohl eindeutigen Inhalt.

Outlook wird weiterhin die e-Mails in einem einzelnen Gespräch Gruppe; nur die letzte e-Mail-Nachrichten lesen bedeutet fehlende im Kontext der e-Mail vorletzten, die auch eindeutigen Inhalt enthält. Da threading-e-Mail, jede e-Mail in einzelne Komponenten analysiert und miteinander verglichen, würde threading-e-Mail-Markieren beider die letzten beiden e-Mails als Inclusives, um sicherzustellen, dass Sie alle Kontext verpassen, solange Sie alle e-Mails als inklusive markiert gelesen.