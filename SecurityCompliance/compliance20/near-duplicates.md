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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 40270fa1e3a6f7cdf0dd2a83650aa36a935d9a6d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213125"
---
# <a name="near-duplicate-detection"></a>Erkennen von Quasiduplikaten

Betrachten Sie eine Gruppe von Dokumenten, die überprüft werden sollen, wobei eine Teilmenge auf derselben Vorlage basiert und größtenteils die gleiche Standardsprache hat, mit ein paar unterschieden hier und dort. Wenn ein Prüfer diese Teilmenge identifizieren, eine gründlich überprüfen und die Unterschiede für den Rest überprüfen könnte, würden Sie keine eindeutigen Informationen verpasst haben, während Sie nur einen Bruchteil der Zeit, die Sie dazu ergriffen hätte, alle Dokumente zu decken lesen. In der Nähe von doppelten Erkennungs Gruppen werden Text ähnliche Dokumente zusammengeführt, damit Sie den Überprüfungsprozess effizienter gestalten können.

## <a name="how-does-it-work"></a>Wie funktioniert dies?

Wenn die Erkennung nahezu doppelt ausgeführt wird, analysiert das System jedes Dokument mit Text. Dann vergleicht es jedes Dokument gegeneinander, um zu bestimmen, ob Ihre Ähnlichkeit größer als der festgelegte Schwellenwert ist. Wenn dies der Fall ist, werden die Dokumente gruppiert. Nachdem alle Dokumente verglichen und gruppiert wurden, wird ein Dokument aus jeder Gruppe als "Pivot" markiert; Wenn Sie Ihre Dokumente überprüfen, können Sie zuerst ein Pivot überprüfen und die anderen Dokumente in derselben fast doppelt vorhandenen Gruppe überprüfen, wobei der Fokus auf dem Unterschied zwischen dem Pivot und dem Dokument liegt, das sich im Rückblick befindet.