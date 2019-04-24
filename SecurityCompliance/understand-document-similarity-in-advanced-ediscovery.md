---
title: GrundLegendes zur Dokument Ähnlichkeit in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Überprüfen Sie, wie der Wert der Dokument Ähnlichkeit, der minimale Grad an Ähnlichkeit für zwei Dateien, die als near-Duplikate betrachtet werden, in Office 365 Advanced eDiscovery verwendet werden kann. '
ms.openlocfilehash: eb8f07ceedb10bd0152693dd1e82a28797d86a5a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264147"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>GrundLegendes zur Dokument Ähnlichkeit in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Bei Advanced eDiscovery ist die Dokument Ähnlichkeit die minimale Ähnlichkeits Stufe, die erforderlich ist, damit zwei Dokumente als nahezu Duplikate betrachtet werden.
  
> [!TIP]
> Für die meisten Geschäftsanwendungen empfiehlt es sich, einen Ähnlichkeitswert von 60%-75% zu verwenden. Bei sehr schlechter Qualität der optischen Zeichenerkennung (OCR) können niedrigere Ähnlichkeitswerte angewendet werden. 
  
> [!NOTE]
> Nachdem er für einen bestimmten Fall festgelegt und ausgeführt wurde, kann der Ähnlichkeitswert nicht geändert werden. 
  
In einem near-Duplicate-Satz (ND) kann es Dokumente mit einer Ähnlichkeits Ebene unterhalb des Schwellenwerts für Ähnlichkeit geben. Damit ein Dokument einem ND-Satz beitreten kann, muss mindestens ein Dokument im ND-Satz mit einer Ähnlichkeits Ebene vorhanden sein, die die Ähnlichkeit überschreitet. 
  
Nehmen wir beispielsweise an, dass die Ähnlichkeit auf 80% festgelegt ist, Dokument F1 ähnelt dem Dokument F2 auf einer Ebene von 85%, und Dokument F2 ähnelt dem Dokument F3 auf einer Ebene von 90%. 
  
Dokument F1 ähnelt jedoch möglicherweise Dokument F3 auf einer Ebene von nur 70%, die unterhalb des Schwellenwerts liegt. In diesem Beispiel werden jedoch alle Dokumente F1, F2 und F3 in der einen ND-Gruppe angezeigt. In ähnlicher Weise haben wir mit einem Ähnlichkeitswert von 80% zwei Sätze erstellt: EquiSet-1 und EquiSet-2. EquiSet-1 enthält Dokumente E1 und E2. Equiset-2 enthält die Dokumente F1, F2 und F3. 
  
Die Ähnlichkeits Stufen werden wie folgt dargestellt:
  
![Dokument Ähnlichkeit](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
Gehen Sie davon aus, dass jetzt ein anderes Dokument, x1, eingefügt wird. Die Ähnlichkeit zwischen x1 und E3 beträgt 87%. Entsprechend ist die Ähnlichkeit zwischen x1 und F1 92%. Daher werden EquiSet-1, EquiSet-2 und x1 jetzt zu einem ND-Satz zusammengefasst.
  
![Dokument Ähnlichkeit](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> Wenn zwei Dokumente einem ND-Satz zugewiesen werden, bleiben Sie im gleichen ND-Satz zusammen, auch wenn zusätzliche Dokumente zum Satz hinzugefügt werden oder wenn die Sätze zusammengeführt werden. 
  
Nach dem Zusammenführen von Sätzen kann sich das Pivot-Dokument ändern, wenn neue Dokumente zu einem Satz hinzugefügt werden. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Festlegen von Analyseoptionen](set-analyze-options-in-advanced-ediscovery.md)
  
[Festlegen des Texts ignorieren](set-ignore-text-in-advanced-ediscovery.md)
  
[Einstellung "Erweiterte Einstellungen analysieren"](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Anzeigen von Analyseergebnissen](view-analyze-results-in-advanced-ediscovery.md)

