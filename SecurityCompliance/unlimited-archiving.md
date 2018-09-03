---
title: Übersicht über die uneingeschränkte Archivierung in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Erfahren Sie mehr über automatisch erweitert die Archivierung in Office 365, unbegrenzte Archivierung für Exchange Online-Postfächer enthält.
ms.openlocfilehash: a762a0fb8295a645957404c1c88881f40329f7a1
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782122"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Übersicht über die uneingeschränkte Archivierung in Office 365

In Office 365 bieten archivpostfächer den Benutzern zusätzliche Postfach Speicherplatz. Nach dem Postfach eines Benutzers Archivieren aktiviert ist, ist bis zu 100 GB zusätzlicher Speicher verfügbar. Wenn das Speicherkontingent 100 GB erreicht ist, mussten wenden Sie sich an Microsoft zu Anforderung zusätzlicher Speicherplatz für ein Archivpostfach Organisationen. Dies ist nicht mehr der Fall. Das neue Feature der unbegrenzte Archivierung in Office 365 (bezeichnet *Archivierung erweiterbares*) bietet eine unbegrenzte an Speicherplatz in archivpostfächer. Nun, wenn das Speicherkontingent in das Archivpostfach erreicht ist, Office 365 wird automatisch erhöht, die Größe des Archivs, d. h., Benutzer werden nicht, nicht genügend Speicherplatz Postfach ausgeführt und Administratoren nicht zusätzlichen Speicher für archivpostfächer anfordern müssen .
  
Für eine schrittweise Anleitung zum Aktivieren der automatischen Erweitern Archivierung, finden Sie unter [Aktivieren unbegrenzte Archivierung in Office 365](enable-unlimited-archiving.md).
  
> [!NOTE]
> Erweiterbares auch Archivierung unterstützt freigegebene Postfächer. Um das Archiv für ein freigegebenes Postfach zu aktivieren, ist eine Lizenz für Exchange Online – Plan 2 oder eine Lizenz Exchange Online – Plan 1 mit Exchange Online-Archivierung-Lizenz erforderlich. 
  
## <a name="how-auto-expanding-archiving-works"></a>Funktionsweise der Archivierung wie erweiterbares

Wie bereits erklärt, zusätzliche Postfach wird Speicherplatz erstellt, wenn Archivpostfach des Benutzers aktiviert ist. Erweiterbares Archivierung aktiviert, prüft die Office 365 in regelmäßigen Abständen die Größe des archivpostfachs. Wenn ein Archivpostfach erreicht bald Speichergrenzwert erhält, erstellt Office 365 automatisch zusätzlicher Speicherplatz für das Archiv. Wenn der Benutzer nicht genügend diese zusätzlichen Speicherplatz ausgeführt wird, fügt Office 365 mehr Speicherplatz in Archiv des Benutzers an. Dieser Prozess wird automatisch, was bedeutet, dass Administratoren anfordern zusätzliche Archivspeicher oder Verwalten der Archivierung automatisch erweitert haben. 
  
Nachfolgend finden Sie ein schnellen Überblick über den Prozess.
  
![Übersicht über die Archivierung automatisch erweitert](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. Archivierung ist für ein Benutzerpostfach oder ein freigegebenes Postfach aktiviert. Ein Archivpostfach mit 100 GB freier Speicherplatz wird erstellt, und das Warnung Kontingent für das Archivpostfach auf 90 GB festgelegt ist.
    
2. Ein Administrator kann erweiterbares Archivierung für das Postfach. Klicken Sie dann, wenn das Archivpostfach (einschließlich des Ordners wiederherstellbare Elemente) 90 GB erreicht, wird es in einem Archiv erweiterbares konvertiert und Office 365 fügt Speicherplatz in das Archiv. Beachten Sie, dass dauert bis zu 30 Tage für den zusätzlichen Speicherplatz bereitgestellt werden.
    
3. Office 365 fügt mehr Speicherplatz automatisch in das Archiv bei Bedarf.
  
> [!IMPORTANT]
> Wenn ein Postfach in die Warteschleife gestellt oder um eine Aufbewahrungsrichtlinie für Office 365 zugeordnet ist, wird das Speicherkontingent für die Archivierung Maibox auf 110 GB erhöht, wenn erweiterbares Archivierung aktiviert ist. Auf ähnliche Weise wird die Kontingentgrenzwert auf 100 GB erhöht.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>Was wird auf den Speicherplatz zusätzliche Archiv verschoben?

Um Archivspeicher erweiterbares effizient zu nutzen, möglicherweise Ordner verschoben werden. Office 365 wird bestimmt, welche Ordner verschoben, wenn das Archiv zusätzlicher Speicher hinzugefügt wird. Wenn ein Ordner verschoben wird, wird automatisch ein Unterordner unter dem ursprünglichen Ordner im Archiv Teil der Ordnerliste in Outlook erstellt. Diese neue Unterordner verweist auf die Elemente, die verschoben wurden. Die Benennungskonvention, die Office 365 wird verwendet, um nennen Sie diesen Ordner ist ** \<Ordnername\>_yyyy (auf erstellt mmm TT, JJJJ H_mm)**, wobei: 
  
- **JJJJ** ist das Jahr, den, das die Nachrichten im Ordner empfangen wurden. 
    
- **mmm TT, JJJJ H_m** ist das Datum und die Uhrzeit, die der Unterordner von Office 365, im UTC-Format, basierend auf der Zeitzone des Benutzers und der regionalen Einstellungen in Outlook erstellt wurde. 
    
Die folgenden Screenshots anzeigen eine Ordnerliste vor und nach Nachrichten in einem Archiv automatisch erweitert verschoben werden.
  
 **Vor dem Hinzufügen zusätzlichen Speichers**
  
![Ordnerliste Archivpostfach bevor erweiterbares Archiv bereitgestellt ist.](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **Nach dem Hinzufügen zusätzlichen Speichers**
  
![Ordnerliste Archivpostfach nach erweiterbares Archiv bereitgestellt ist.](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>Outlook-Anforderungen für den Zugriff auf Elemente in einem Archiv automatisch erweitert

Um Nachrichten zugreifen, die in einem Archiv automatisch erweitert gespeichert sind, müssen Benutzer eine der folgenden Outlook-Clients verwenden:
  
- Outlook 2016 für Windows
    
- Outlook im Web 
    
- Outlook 2016 für Mac 
    
> [!NOTE]
> Outlook 2013-Benutzer können nur Zugriff auf Elemente, die ursprünglich in ihre Archivpostfach gespeichert wurden. Sie werden kann nicht für den Zugriffselemente, die in zusätzliche Archivspeicher verschoben werden. 
  
Hier sind einige Punkte, berücksichtigen Sie beim Verwenden von Outlook oder Outlook im Web zum Zugriff auf Nachrichten in einem Archiv automatisch erweitert gespeichert.
  
- Sie können ein beliebiger Ordner im Archivpostfach, einschließlich Schriftarten, die in den Bereich für die automatische erweiterte Speicherung verschoben wurden zugreifen.
    
- Sie können nach Elementen suchen, die in einen Bereich zusätzlicher Speicher verschoben wurden, nur, indem Sie den Ordner selbst suchen. Dies bedeutet, dass Sie den Archivordner in Ordnerliste, um die **Aktuellen Ordner** als den Suchbereich auswählen aus. Enthält ein Ordner in einem automatisch erweitert Speicherbereich Unterordner, müssen Sie auf ähnliche Weise jedem Unterordner separat zu suchen. 
    
- Anzahl der Element in Outlook und Lese-/ungelesen zählt (in Outlook und Outlook im Web) in einem Archiv automatisch erweitert ist möglicherweise nicht korrekt.
    
- Sie können Löschen von Elementen in einem Unterordner, der auf einen Speicherbereich automatische erweitert verweist, aber der Ordner selbst kann nicht gelöscht werden.
    
- Sie können das Feature gelöschte Elemente wiederherstellen Wiederherstellen eines Elements, das in einem Speicher automatisch erweitert gelöscht wurde.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>Erweiterbares Archivierung und andere Office 365 Compliance-features

In diesem Abschnitt wird die Funktionalität zwischen erweiterbares Archivierung und andere Office 365 Compliance und Daten Governance Features erläutert.
  
- **eDiscovery** - bei Verwendung ein Office 365 eDiscovery-Tools, z. B. Inhaltssuche oder Compliance-eDiscovery, die Bereiche zusätzlicher Speicher in einem Archiv automatisch erweitert werden ebenfalls durchsucht.
    
- **Aufbewahrung** - Wenn Sie ein Postfach gehalten in Exchange Online mithilfe von Tools wie Aufbewahrung für eventuelle Rechtsstreitigkeiten oder eDiscovery-Fall Archive und Aufbewahrungsrichtlinien in die Office 365-Sicherheit &amp; Compliance Center, Inhalt befindet sich in einem Archiv automatisch erweitert ist auch in der Warteschleife platziert.
    
- **Messaging-datensatzverwaltung (MRM)** - Wenn Sie Löschrichtlinien MRM in Exchange Online verwenden, um abgelaufene Postfachelemente, befindet sich im Archiv automatisch erweitert abgelaufene Elemente endgültig löschen, werden ebenfalls gelöscht.
    
- **Importieren von Dienst** - Sie können den Dienst Office 365 importieren zum Importieren von PST-Dateien des Benutzers automatisch erweitert Archiv verwenden. Sie können bis zu 100 GB an Daten aus PST-Dateien in Archivpostfach des Benutzers importieren. 

## <a name="more-information"></a>Weitere Informationen

Ausführliche technische Informationen zur Archivierung, finden Sie unter erweiterbares [Office 365: Archive – häufig gestellte Fragen erweiterbares](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).