---
title: Anzeigen von Ergebnisse der Analyse in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Verstehen Sie, wo Sie die Ergebnisse der Analyse abgeschlossen in Office 365 erweiterte eDiscovery, einschließlich der Definitionen von der angezeigten Aufgabenoptionen anzuzeigen.  '
ms.openlocfilehash: 8f1de53e5548c8721f8fbfdb83374edb18379114
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529837"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a>Anzeigen von Ergebnisse der Analyse in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Im erweiterten eDiscovery können Status und die Ergebnisse für die Analyse-Prozess in einer Vielzahl von zeigt angezeigt werden, wie unten beschrieben.
  
## <a name="view-analyze-task-status"></a>Anzeigen des Status der Analyse-Aufgabe

In **Prepare \> Analyze \> Ergebnisse \> Taskstatus**, der Status wird angezeigt, während und nach der Ausführung der Analyse-Prozesses. 
  
![Aufgabenstatus analysieren](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
Die angezeigten Aufgaben variieren je nach den ausgewählten Optionen. 
  
- **ND/ET: Setup**: Beispiel für die Ausführung vorbereitet, ausführen und die Groß-/Kleinschreibung-Parameter festgelegt.
    
- **ND/ET: ND Berechnung**: Prozesse nahezu doppelte Analyse der Dateien.
    
- **ND/ET: ET Berechnung**: Analyse auf die gesamte e-Mail-Satz E-Mail-Thread ausgeführt wird.
    
- **ND/ET: Pivot-Elemente und gemeinsamkeiten**: führt die Pivot und Verarbeitung von Ähnlichkeit.
    
- **ND/ET: Metadaten Update**: Schließt die neuen Daten, die für die Dateien in der Datenbank erfasst.
    
- **Designs: Designs Berechnung**: führt Designs Analyse. (Nur wenn aktiviert angezeigt.)
    
- **Aufgabenstatus**: Diese Zeile wird nach Abschluss des Tasks angezeigt. Während der Ausführung der Aufgaben, wird zur Dauer angezeigt.
    
> [!NOTE]
> Die Analyse Ergebnisse der in der Nähe Duplikate und e-Mail-Threads (ND und ED) gilt für die Anzahl der Dokumente verarbeitet werden. Es ist nicht genaue duplizierte Dateien enthalten. 
  
## <a name="view-near-duplicates-and-email-threads-status"></a>Anzeigen des Status von in Ihrer Nähe Duplikate und e-Mail-Threads

Die **Ziel** -Auffüllung Ergebnisse anzeigen der Anzahl von Dokumenten, e-Mails, Anlagen und Fehler in die Zielgruppe. 
  
Die **Dokumente** Ergebnisse anzeigen der Anzahl von Pivot-Elemente in der Nähe Duplikate eindeutige und genauen duplizierten Dateien. 
  
Die Ergebnisse **-e-Mails** zeigt die Anzahl der inklusive, inklusive minus eindeutige inklusive Kopien und den Rest der e-Mail-Nachrichten. Die verschiedenen Typen von e-Mail-Ergebnisse sind: 
  
- **Inklusive**: eine inklusive e-Mail ist der abschließende Knoten in einer e-Mail-Thread und den vorherigen Verlauf von diesem Thread enthält. Der Prüfer kann daher sicher auf die inklusive e-Mail, ohne die Notwendigkeit, lesen Sie die vorherigen Nachrichten in der Thread konzentrieren. 
    
- **Inklusive minus**: eine inklusive e-Mail wird als inklusive Minuszeichen gekennzeichnet, wenn Sie eine oder mehrere verschiedene Anlagen, die die übergeordneten Elemente der inklusive Nachricht zugeordnet sind. In dieser bestimmten inklusive e-Mail enthalten Kontext, sich der Begriff, den übergeordneten für Nachrichten, die sich nicht auf die e-Mail-Thread oder Unterhaltungen nach oben verwendet wird, in diesem. Bearbeiter kann die inklusive minus Angabe als Signal verwenden, obwohl es nicht notwendig, den Inhalt der übergeordneten Speicherorte inklusive e-Mail überprüfen möglicherweise, überprüfen Sie die Anlagen der Eltern inklusive Pfad zugeordnet werden. 
    
- **Inklusive Kopie**: eine inklusive e-Mail wird als inklusive Kopie ist die Kopie einer anderen Nachricht wie inklusive oder minus inklusive gekennzeichnet festgelegt. Anders ausgedrückt, diese Meldung hat den gleichen Betreff und Text als eine andere Nachricht inklusive und als solche in demselben Knoten gemeinsame befindet. Da inklusive Kopie Nachrichten denselben Inhalt enthalten, können sie in der Regel bei der Überprüfung übersprungen werden. 
    
- **Die restlichen**: e-Mail, die nicht eindeutige Inhalte enthalten, und daher nicht fallen in eine der vorherigen drei Kategorien angegeben. Diese e-Mail-Nachrichten müssen nicht überprüft werden. Wenn eine Nachricht eine Anlage, die eine weiter unten inklusive e-Mail nicht ist enthält, müssen die Anlage überprüft werden. Dies wird durch das Vorhandensein einer inklusive minus e-Mail innerhalb des Threads angegeben.
    
Die **Anlagen** Ergebnisse anzeigen der Anzahl von Anlagen an, entsprechend solche Typ als eindeutig und Duplikate. 
  
![Nahe Duplikate und E-Mail-Threads](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zu Dokument Ähnlichkeit](understand-document-similarity-in-advanced-ediscovery.md)
  
[Festlegen von Optionen für Analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Die Einstellung Text ignorieren](set-ignore-text-in-advanced-ediscovery.md)
  
[Analysieren der Einstellung Erweiterte Einstellungen](view-analyze-results-in-advanced-ediscovery.md)

