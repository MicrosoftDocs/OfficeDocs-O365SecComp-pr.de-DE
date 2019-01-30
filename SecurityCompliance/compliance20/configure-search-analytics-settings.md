---
title: Konfigurieren der Suche und-Analyse
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
ms.openlocfilehash: d9528a4bcfaa77f2e232b25d03eda46cce42ebb9
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607787"
---
# <a name="configure-search-and-analytics-settings"></a>Konfigurieren der Suche und-Analyse


## <a name="near-duplicates-and-email-threading"></a>In der Nähe von Duplikaten und threading-e-Mail

In diesem Abschnitt können Sie die Parameter für die Erkennung von Duplikaten, in der Nähe Erkennung von Duplikaten und e-Mail-threading festlegen.

- Aktivieren/deaktivieren: enthalten Sie Erkennung von Duplikaten, in der Nähe Erkennung von Duplikaten und e-Mail-threading als Teil des Analytics Ablauf aktiviert. Da sie übereinander erstellen, müssen Sie alle diese aktivieren oder Deaktivieren aller Folien.

- Schwellenwert: Wenn die Ebene der Ähnlichkeit von zwei Dokumenten oberhalb der Schwelle sind, werden sie in der gleichen nahezu doppelte Set versetzt.

- Ausblenden von Duplikaten standardmäßig: Wenn diese Einstellung aktiviert ist, wird ein Filter, um doppelte Dokumente ausblenden in die Arbeitsseiten standardmäßig angewendet werden. Der Filter kann manuell in die Arbeitsseiten bei Bedarf entfernt werden.

- Minimale/maximale Anzahl von Wörtern: in der Nähe von Duplikaten und e-Mail-threading nur bei Dokumenten mit mindestens die minimale Anzahl von Wörtern und höchstens die maximale Anzahl von Wörtern ausgeführt wird. Weitere Informationen finden Sie [in der Nähe Erkennung von Duplikaten](near-duplicates.md) und [threading-e-Mail](email-threading.md).

## <a name="themes"></a>Designs

In diesem Abschnitt können Sie die Parameter für Designs festlegen.

- Aktivieren/deaktivieren: enthalten Sie Designs clustering als Teil des Analytics Ablauf aktiviert.
- Maximale Anzahl von Designs dynamisch dynamisch anpassen: in bestimmten Fällen sind nicht genügend Dokumente, um die gewünschte Anzahl von Designs zu erstellen. Wenn diese Einstellung aktiviert ist, klicken Sie dann statt So erzwingen Sie die gewünschte maximale Anzahl von Designs, versucht das System maximale Anzahl von Designs passt dynamisch an.
- Maximale Anzahl von Designs: gewünschte Anzahl der Designs
- Zahlen in Designs enthalten: Wenn aktiviert, wird es Zahlen in einschließen, wenn Designs zu generieren.  

## <a name="optical-character-recognition-ocr"></a>Optische zeichenerkennung (OCR)

Wenn diese Einstellung aktiviert ist, wird OCR auf Bilder ausgeführt werden, die in Arbeitsseiten aufgenommen werden, damit sie durchsucht werden können.

## <a name="ignore-text"></a>Ignorieren von text

Es gibt Situationen, in dem bestimmte Texte die Qualität der Analyse, wie lange Haftungsausschlüssen abnehmen, die auf bestimmte unabhängig vom Inhalt der e-Mail-e-Mails hinzugefügt werden. Wenn Sie solchen Fällen kennen, können Sie diesen Text aus Analytics ausschließen, indem Text (RegEx wird unterstützt) und dem angibt Module, die für Text ausgeschlossen werden soll.