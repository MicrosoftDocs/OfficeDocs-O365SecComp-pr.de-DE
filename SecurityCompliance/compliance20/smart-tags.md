---
title: Einrichten von Smarttags für die Erkennung von Anwalts-Client-Berechtigungen in Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 5310acad1aa1bc2e01cbabee69dd7bb38084bd9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153967"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a>Einrichten von Smarttags für die ml-unterstützte Überprüfung in Advanced eDiscovery

Maschinelle Lernfunktionen in Advanced eDiscovery sollen helfen, den Entscheidungsprozess in Dokumenten effizienter zu gestalten. Smarttags sind eine Möglichkeit, die Lernfunktionen des Computers in die Position zu versetzen, an der die Entscheidungen erfasst werden: Tags und Tag-Gruppen. Wenn Sie eine smarttaggruppe erstellen, werden die Entscheidungen des ml-Modells, das der Gruppe zugeordnet ist, Inline mit den Tags in der Gruppe angezeigt, damit Sie die Informationen Inline anzeigen können, wo Sie am ehesten Sinn ergeben.

## <a name="how-to-set-up-a-smart-tag-group"></a>Vorgehensweise Einrichten einer smarttaggruppe

1. Wechseln Sie in einem Überprüfungs Satzes zu **Manage Review-Gruppe** -> **Manage Tags**.

2. Klicken Sie auf die Dropdownliste neben **Transpondergruppe hinzufügen** , und wählen Sie **smarttaggruppe hinzufügen**aus.

3. Wählen Sie das Modell aus, das Sie dieser Gruppe zuordnen möchten. Dadurch werden ein Tag-Abschnitt und n untergeordnete Tags erstellt, wobei n für die Anzahl der möglichen Ausgaben des Modells steht. Beispielsweise weist das Client-Berechtigungs Erkennungs Modell zwei mögliche Ausgaben auf – privilegierte und nicht privilegierte; durch die Auswahl dieses Modells werden zwei untergeordnete Tags in der Überprüfungsgruppe erstellt, die jeweils einer der möglichen Ausgaben entsprechen.

4. Benennen Sie die Transpondergruppe und die Tags entsprechend ihrer Größe um.

## <a name="how-to-use-a-smart-tag-group"></a>Vorgehensweise verwenden einer smarttaggruppe

Wenn Sie ein Dokument überprüfen, werden die Ergebnisse des Modells neben dem entsprechenden Transponderwert verfügbar gemacht. Wenn Sie beispielsweise über eine smarttaggruppe für die Erkennung von Anwalts-und Client Rechten verfügen und ein Dokument überprüfen, das das Modell als potenziell privilegiert hat, wird der Grund dafür neben dem entsprechenden Tag angezeigt. Es ist wichtig zu beachten, dass das Tag nicht automatisch angewendet wird; für alle Absichten und Zwecke fungieren Tags innerhalb einer smarttaggruppe genauso wie normale Tags, mit dem Unterschied, dass Sie die Modellergebnisse neben Ihnen verfügbar machen, wenn dies angemessen ist.