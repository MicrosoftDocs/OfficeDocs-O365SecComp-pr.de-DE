---
title: Erkennen von Quasiduplikaten
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
ms.openlocfilehash: 941809193a3342d8c7b9de991370848aee4af070
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030149"
---
# <a name="near-duplicate-detection"></a>Erkennen von Quasiduplikaten

Betrachten Sie eine Gruppe von Dokumenten, die überprüft werden sollen, wobei eine Teilmenge auf derselben Vorlage basiert und größtenteils die gleiche Standardsprache hat, mit ein paar unterschieden hier und dort. Wenn ein Prüfer diese Teilmenge identifizieren, eine gründlich überprüfen und die Unterschiede für den Rest überprüfen könnte, würden Sie keine eindeutigen Informationen verpasst haben, während Sie nur einen Bruchteil der Zeit, die Sie dazu ergriffen hätte, alle Dokumente zu decken lesen. In der Nähe von doppelten Erkennungs Gruppen werden Text ähnliche Dokumente zusammengeführt, damit Sie den Überprüfungsprozess effizienter gestalten können.

## <a name="how-does-it-work"></a>Wie funktioniert dies?

Wenn die Erkennung nahezu doppelt ausgeführt wird, analysiert das System jedes Dokument mit Text. Dann vergleicht es jedes Dokument gegeneinander, um zu bestimmen, ob Ihre Ähnlichkeit größer als der festgelegte Schwellenwert ist. Wenn dies der Fall ist, werden die Dokumente gruppiert. Nachdem alle Dokumente verglichen und gruppiert wurden, wird ein Dokument aus jeder Gruppe als "Pivot" markiert; Wenn Sie Ihre Dokumente überprüfen, können Sie zuerst ein Pivot überprüfen und die anderen Dokumente in derselben fast doppelt vorhandenen Gruppe überprüfen, wobei der Fokus auf dem Unterschied zwischen dem Pivot und dem Dokument liegt, das sich im Rückblick befindet.