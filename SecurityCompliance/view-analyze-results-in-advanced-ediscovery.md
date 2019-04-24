---
title: Anzeigen von Analyseergebnissen in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Hier erfahren Sie, wo die Ergebnisse des Analyseprozesses in Office 365 Advanced eDiscovery angezeigt werden, einschließlich Definitionen der angezeigten Aufgabenoptionen.  '
ms.openlocfilehash: 990bcbb3c6626521d40f7ce057c764200d5047b5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267105"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a>Anzeigen von Analyseergebnissen in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In Advanced eDiscovery können Fortschritte und Ergebnisse für den Analyseprozess in einer Vielzahl von Displays angezeigt werden, wie unten beschrieben.
  
## <a name="view-analyze-task-status"></a>Anzeigen des Vorgangsstatus

In **Prepare \> analyze \> results \> Task Status**wird der Status während und nach der Analyse der Prozessausführung angezeigt. 
  
![Aufgabenstatus analysieren](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
Welche Aufgaben angezeigt werden, hängt von den ausgewählten Optionen ab. 
  
- **ND/et: Setup**: Prepares for the Run, beispielsweise legt die Parameter Run und Case fest.
    
- **ND/et: ND-Berechnung**: verarbeitet die nahezu duplizierte Analyse von Dateien.
    
- **ND/et: et-Berechnung**: führt eine e-Mail-Thread Analyse für den gesamten e-Mail-Satz durch.
    
- **ND/et: Pivots und Ähnlichkeiten**: führt Pivot-und Datei Ähnlichkeits Verarbeitung aus.
    
- **ND/et: Metadata Update**: finalisiert die neuen Daten, die für die Dateien in der Datenbank gesammelt werden.
    
- **Designs: Design Berechnung**: führt die Design Analyse aus. (Nur angezeigt, wenn ausgewählt.)
    
- **Vorgangsstatus**: diese Leitung wird nach Abschluss der Aufgabe angezeigt. Während Vorgänge ausgeführt werden, wird die Ausführungsdauer angezeigt.
    
> [!NOTE]
> Die Analyseergebnisse von Near-Duplikaten und e-Mail-Threads (ND und ED) beziehen sich auf die Anzahl der zu verarbeitenden Dokumente. Es enthält nicht exakte Duplikatdateien. 
  
## <a name="view-near-duplicates-and-email-threads-status"></a>Anzeigen von Near-Duplikaten und e-Mail-Threads Status

Die Ergebnisse der **Ziel** Auffüllung zeigen die Anzahl von Dokumenten, e-Mails, Anlagen und Fehlern in der Zielauffüllung an. 
  
Die Ergebnisse der **Dokumente** zeigen die Anzahl der Pivots, die eindeutigen Duplikate und die exakten doppelten Dateien an. 
  
In **** den e-Mail-Ergebnissen wird die Anzahl der inklusiv-inklusive-minus-, Unique-inklusive-Kopien und die restlichen e-Mails angezeigt. Die verschiedenen Typen von e-Mail-Ergebnissen sind: 
  
- **Inclusive**: eine inklusive e-Mail ist der abschließende Knoten in einem e-Mail-Thread und enthält alle vorherigen Verlauf dieses Threads. Daher kann der Prüfer sich sicher auf die inklusive e-Mail konzentrieren, ohne die vorherigen Nachrichten im Thread lesen zu müssen. 
    
- **Inklusive minus**: eine inklusiv-e-Mail wird als inklusive minus festgelegt, wenn es eine oder mehrere verschiedene Anlagen gibt, die den Eltern der Inclusive-Nachricht zugeordnet sind. In diesem Kontext wird der Begriff Parent für Nachrichten verwendet, die sich nach oben im e-Mail-Thread oder Unterhaltungen befinden, die in dieser spezifischen inclusive-e-Mail enthalten sind. Ein Prüfer kann die inklusive minus-Anzeige als Signal verwenden, dass es zwar nicht notwendig ist, den Inhalt der inklusiven e-Mail-Eltern zu überprüfen, es jedoch hilfreich sein kann, die Anlagen zu überprüfen, die mit den übergeordneten Pfad-Eltern verknüpft sind. 
    
- **Inklusive Kopie**: eine inklusiv-e-Mail wird als inklusive Kopie festgelegt, wenn es sich um die Kopie einer anderen Nachricht handelt, die als inklusive oder inklusive minus gekennzeichnet ist. Anders ausgedrückt: Diese Nachricht hat denselben Betreff und Text wie eine andere inklusive Nachricht und befindet sich als solche im gleichen Knoten. Da inclusive Copy-Nachrichten denselben Inhalt enthalten, können Sie in der Regel beim Überprüfungsprozess übersprungen werden. 
    
- **Der Rest**: Dies gibt e-Mails an, die keinen eindeutigen Inhalt enthalten und daher nicht in eine der vorherigen drei Kategorien fallen. Diese e-Mail-Nachrichten müssen nicht überprüft werden. Wenn eine Nachricht eine Anlage enthält, die nicht in einer späteren inclusive-e-Mail enthalten ist, muss die Anlage möglicherweise überprüft werden. Dies wird durch das vorhanden sein einer inklusiven minus-e-Mail innerhalb des Threads angezeigt.
    
Die Ergebnisse der **Anlagen** zeigen die Anzahl der Anlagen gemäß diesem Typ als Unique und Duplikate an. 
  
![Near-Duplikate und e-Mail-Threads](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Dokument Ähnlichkeit](understand-document-similarity-in-advanced-ediscovery.md)
  
[Festlegen von Analyseoptionen](set-analyze-options-in-advanced-ediscovery.md)
  
[Festlegen des Texts ignorieren](set-ignore-text-in-advanced-ediscovery.md)
  
[Einstellung "Erweiterte Einstellungen analysieren"](view-analyze-results-in-advanced-ediscovery.md)

