---
title: Einrichten von Smarttags für die Rechtsanwalt-Erkennung von Client Rechten in Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 721426f23aec862bcefbd13b8e61415dac3aeb27
ms.sourcegitcommit: aa8ea45d5854f8906714e0a407937585ec7993ad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33951699"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a>Einrichten von Smarttags für die ml-gestützte Überprüfungen in Advanced eDiscovery

Maschinelle Lernfunktionen in Advanced eDiscovery sollen dazu beitragen, den Entscheidungsprozess für Dokumente effizienter zu gestalten. Smarttags sind eine Möglichkeit, um die Computer Lernfunktionen in den Bereichen zu integrieren, in denen die Entscheidungen aufgezeichnet werden: Tags und Tag-Gruppen. Wenn Sie eine smarttaggruppe erstellen, werden die Entscheidungen des ml-Modells, das der Gruppe zugeordnet ist, Inline mit den Tags in der Gruppe angezeigt, damit Sie die Informationen Inline sehen können, wo Sie im Kontext am sinnvollsten sind.

## <a name="how-to-set-up-a-smart-tag-group"></a>Einrichten einer smarttaggruppe

1. Gehen Sie in einem Übersichts Satz zu **Manage Review Set** -> **Manage Tags**.

2. Klicken Sie auf die Dropdownliste neben **Tag hinzufügen** , und wählen Sie **smarttaggruppe hinzufügen**aus.

3. Wählen Sie das Modell aus, das Sie dieser Gruppe zuordnen möchten. Dadurch werden ein Tag-Abschnitt und n untergeordnete Tags erstellt, wobei n die Anzahl der möglichen Ausgaben des Modells ist. Beispielsweise hat das "Attorney-Client-Berechtigungs Erkennungs Modell" zwei mögliche Ausgänge-privileged und nicht privilegierte; Bei Auswahl dieses Modells werden zwei untergeordnete Tags im Übersichts Satz erstellt, die jeweils einer der möglichen Ausgaben entsprechen.

4. Benennen Sie die beschriftungsgruppe und die Markierungen entsprechend um.

## <a name="how-to-use-a-smart-tag-group"></a>Verwenden einer smarttaggruppe

Beim Überprüfen eines Dokuments werden die Ergebnisse des Modells neben dem entsprechenden Tag-Wert angezeigt. Wenn Sie beispielsweise über eine smarttaggruppe für die Erkennung von Anwalts-und Clientberechtigungen verfügen und Sie ein Dokument überprüfen, das das Modell als potenziell privilegiert festgelegt hat, sehen Sie den Grund dafür neben dem entsprechenden Tag. Beachten Sie, dass das-Tag nicht automatisch angewendet wird. in allen Absichten und Zwecken fungieren Tags innerhalb einer smarttaggruppe genau wie normale Tags, mit dem Unterschied, dass Sie bei Bedarf die Modellergebnisse offen legen.