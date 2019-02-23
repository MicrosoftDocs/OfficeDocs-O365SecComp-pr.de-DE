---
title: Konfigurieren der Such- und Analyseeinstellungen
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
ms.openlocfilehash: 253650bb9916da8260491870d1a0bc899d6245c8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217105"
---
# <a name="configure-search-and-analytics-settings"></a>Konfigurieren der Such- und Analyseeinstellungen


## <a name="near-duplicates-and-email-threading"></a>Near-Duplikate und e-Mail-Threading

In diesem Abschnitt können Sie Parameter für die doppelte Erkennung, fast doppelt Erkennung und e-Mail-Threading festlegen.

- Aktivieren/deaktivieren: doppelte Erkennung, Erkennung in der Nähe von Duplikaten und e-Mail-Threading als Teil des Analyse Flusses, falls aktiviert, einbeziehen. Da Sie sich übereinander aufbauen, müssen Sie alle aktivieren oder alle deaktivieren.

- Schwellenwert: Wenn die Ähnlichkeits Stufe zweier Dokumente über dem Schwellenwert liegt, werden Sie in derselben fast doppelt vorhandenen Gruppe platziert.

- Duplikate standardmäßig ausblenden: Wenn diese Einstellung aktiviert ist, wird standardmäßig ein Filter zum Ausblenden doppelter Dokumente angewendet. Der Filter kann bei Bedarf manuell im Arbeitssatz entfernt werden.

- Minimale/maximale Anzahl von Wörtern: in der Nähe von Duplikaten und e-Mail-Threading wird nur für Dokumente ausgeführt, die mindestens die Mindestanzahl von Wörtern und höchstens die maximale Anzahl von Wörtern aufweisen. Weitere Informationen finden Sie unter [near Duplicate Detection](near-duplicates.md) and [Email Threading](email-threading.md).

## <a name="themes"></a>Designs

In diesem Abschnitt können Sie Parameter für Designs festlegen.

- Aktivieren/deaktivieren: Thema-Clustering als Teil des Analyse Flusses einbeziehen, falls aktiviert.
- Stellen Sie die maximale Anzahl von Designs dynamisch dynamisch ein: in bestimmten Fällen gibt es nicht genügend Dokumente, um die gewünschte Anzahl von Designs zu erzeugen. Wenn diese Einstellung aktiviert ist, wird anstelle der gewünschten maximalen Anzahl von Designs das System die maximale Anzahl von Designs dynamisch angepasst.
- Maximale Anzahl von Designs: gewünschte Anzahl von Designs
- Zahlen in Designs einbeziehen: Wenn diese Option aktiviert ist, werden beim Generieren von Designs Zahlen eingeschlossen.  

## <a name="optical-character-recognition-ocr"></a>Optische Zeichenerkennung (OCR)

Wenn diese Einstellung aktiviert ist, wird die OCR auf Bildern ausgeführt, die in Arbeitsmappen aufgenommen werden, damit Sie durchsuchbar werden können.

## <a name="ignore-text"></a>Text ignorieren

Es gibt Fälle, in denen bestimmte Texte die Qualität der Analysen verringern, wie lange Haftungsausschlüsse, die zu bestimmten e-Mails hinzugefügt werden, unabhängig vom Inhalt der e-Mail. Wenn Sie solche Fälle wissen, können Sie diesen Text aus der Analyse ausschließen, indem Sie den Text angeben (RegEx wird unterstützt) und für welche Module Dieser Text ausgeschlossen werden soll.