---
title: Grundlegendes zu Dokument Ähnlichkeit in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Überprüfen Sie die Funktionsweise von Dokument Ähnlichkeit-Wert, der minimale Ebene der Ähnlichkeit für zwei Dateien in Ihrer Nähe Duplikate gezogen werden in Office 365 erweiterte eDiscovery. '
ms.openlocfilehash: 39cd8c31204f0164f6b52c71fa707253cb22758a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529281"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>Grundlegendes zu Dokument Ähnlichkeit in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In erweiterten eDiscovery ist Dokument Ähnlichkeit die minimale Ebene der Ähnlichkeit von zwei Dokumenten berücksichtigt werden, als in der Nähe Duplikate erforderlich.
  
> [!TIP]
> Für die meisten Geschäftsanwendungen wird empfohlen, einen Wert Ähnlichkeit von 60-75 % verwenden. Für sehr niedrige Qualität optischen zeichenerkennung (OCR) Material niedrigerer Ähnlichkeit Werte angewendet werden können. 
  
> [!NOTE]
> Nach dem Festlegen und für einen bestimmten Fall ausgeführt hat, kann der Wert der Ähnlichkeit geändert werden. 
  
Innerhalb eines Satzes Near-Duplicate (ND) möglicherweise Dokumente mit einer Ebene der Ähnlichkeit unter dem Schwellenwert Ähnlichkeit. Für ein Dokument an eine Menge ND teilnehmen muss mindestens ein Dokument in der mit einer Ebene der Ähnlichkeit überschreiten der Ähnlichkeit festlegen ND vorhanden sein. 
  
Nehmen wir beispielsweise an die Ähnlichkeit auf 80 % festgelegt ist, Dokument F1 ähnelt Dokument F2 auf einer Ebene der 85 % und Dokument F2 ähnelt Dokument F3 in Höhe von 90 %. 
  
Dokument F1 kann jedoch Dokument F3 auf einer Ebene nur 70 % ähneln sich unter dem Schwellenwert für handelt. Legen Sie dennoch in diesem Beispiel Dokumente F1, F2 und F3, die alle in der eine ND angezeigt werden. In ähnlicher Weise den Wert 80 % Ähnlichkeit verwenden, wir möglicherweise zwei Sätze, EquiSet-1 und EquiSet-2 erstellt haben. EquiSet-1 enthält Dokumente E1 und E2. Equiset-2 enthält die Dokumente F1, F2 und F3. 
  
Die Ebenen der Ähnlichkeit sind wie folgt dargestellt:
  
![Dokumentähnlichkeit](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
Wird davon ausgegangen Sie, dass ein anderes Dokument, X1, nun eingefügt wird. Der Ähnlichkeit zwischen X1 und E3 ist 87 %. In ähnlicher Weise wird die Ähnlichkeit zwischen X1 und F1 92 %. Daher EquiSet -1,-2 EquiSet und X1 werden jetzt kombiniert in einem ND festgelegt.
  
![Dokumentähnlichkeit](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> Wenn zwei Dokumente sind einem ND Satz zugeordnet, zusammen in den gleichen Satz ND bleiben wird, auch wenn zusätzliche Dokumente werden hinzugefügt, das Festlegen oder die legt zusammengeführt werden. 
  
Nach dem legt zusammengeführt werden, kann das Pivot-Dokument ändern, wenn eine Reihe neuer Dokumente hinzugefügt werden. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Festlegen von Optionen für Analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Die Einstellung Text ignorieren](set-ignore-text-in-advanced-ediscovery.md)
  
[Analysieren der Einstellung Erweiterte Einstellungen](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Anzeigen von Ergebnissen der Analyse](view-analyze-results-in-advanced-ediscovery.md)

