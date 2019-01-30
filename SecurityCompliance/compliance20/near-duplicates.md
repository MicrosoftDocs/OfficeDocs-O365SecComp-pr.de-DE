---
title: Erkennung von Duplikaten in Ihrer Nähe.
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
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607780"
---
# <a name="near-duplicate-detection"></a>Erkennung von Duplikaten in Ihrer Nähe.

Erwägen Sie eine Gruppe von Dokumenten überprüft werden, in denen eine Teilmenge basiert auf derselben Vorlage und hauptsächlich der Textbausteine Sprachversion, mit einigen Unterschieden hier und da hat. Wenn ein Bearbeiter konnte diese Teilmenge zu identifizieren, finden Sie in einem von ihnen sorgfältig, und überprüfen Sie die Unterschiede für den Rest, würden sie nicht eindeutige Informationen verpasste beim Offlineschalten von nur eines Bruchs der Zeit, die alle Dokumente Abdeckung zu Abdeckung lesen hätte. Erkennung von Duplikaten NEAR gruppiert Textbefehl ähnliche Dokumente zusammen, mit denen Sie Ihre Überprüfungsprozess effizienter werden.

## <a name="how-does-it-work"></a>Wie funktioniert dies?

Wenn in Ihrer Nähe Erkennung von Duplikaten ausgeführt wird, analysiert das System jedes Dokument mit Text. Anschließend wird jedes Dokument gegeneinander, um festzustellen, ob ihre Ähnlichkeit größer als der festgelegte Schwellenwert ist verglichen. Es ist, werden die Dokumente zusammengefasst. Nachdem alle Dokumente im Vergleich und gruppiert wurden, wird ein Dokument aus jeder Gruppe als "Pivot"; gekennzeichnet. in Ihre Dokumente überprüfen, können Sie einen Pivot zuerst überprüfen und Lesen Sie die anderen Dokumente in der gleichen nahezu doppelte Set Konzentration auf den Unterschied zwischen den Pivot und das Dokument, das in Review ist.