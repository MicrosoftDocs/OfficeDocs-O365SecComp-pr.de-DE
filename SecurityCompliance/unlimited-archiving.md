---
title: Übersicht über die unbegrenzte Archivierung in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Erfahren Sie mehr über die automatische Erweiterung der Archivierung in Office 365, die unbegrenzten Archivspeicher für Exchange Online-Postfächer bereitstellt.
ms.openlocfilehash: 4ed1260cdf348d0bd29d88952ab69d234f044c26
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296648"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Übersicht über die unbegrenzte Archivierung in Office 365

In Office 365 stellen Archivpostfächer Benutzern zusätzlichen Speicherplatz zur Verfügung. Nachdem das Archivpostfach eines Benutzers aktiviert wurde, stehen bis zu 100 GB zusätzlicher Speicher zur Verfügung. Wenn das 100 GB-Speicherkontingent erreicht ist, mussten Organisationen Microsoft kontaktieren, um zusätzlichen Speicherplatz für ein Archivpostfach anzufordern. Das ist nicht mehr der Fall. Die neue unbegrenzte Archivierungsfunktion in Office 365 (sog. *Auto Expanding*Archiving) bietet eine unbegrenzte Menge an Speicherplatz in archivpostfächern. Wenn nun das Speicherkontingent im Archivpostfach erreicht wird, erhöht Office 365 automatisch die Größe des Archivs, was bedeutet, dass dem Benutzer kein Speicherplatz mehr zur Verfügung steht und Administratoren keinen zusätzlichen Speicher für Archivpostfächer anfordern müssen. .
  
Schrittweise Anleitungen zum Aktivieren der automatischen Erweiterung der Archivierung finden Sie unter [enable Unlimited Archiving in Office 365](enable-unlimited-archiving.md).
  
> [!NOTE]
> Die automatisch wachsende Archivierung unterstützt auch freigegebene Postfächer. Zum Aktivieren des Archivs für ein freigegebenes Postfach ist eine Exchange Online-Lizenz für den Plan 2 oder eine Exchange Online-Plan 1-Lizenz mit einer Exchange Online-Archivierungslizenz erforderlich. 
  
## <a name="how-auto-expanding-archiving-works"></a>FunktionsWeise der automatischen Erweiterung der Archivierung

Wie bereits erläutert, wird zusätzlicher Speicherplatz für Postfächer erstellt, wenn das Archivpostfach eines Benutzers aktiviert ist. Wenn die automatische Erweiterung der Archivierung aktiviert ist, überprüft Office 365 regelmäßig die Größe des Archivpostfachs. Wenn ein Archivpostfach dem Speichergrenzwert in der Nähe entspricht, erstellt Office 365 automatisch zusätzlichen Speicherplatz für das Archiv. Wenn der Benutzer diesen zusätzlichen Speicherplatz ausgeht, fügt Office 365 mehr Speicherplatz zum Archiv des Benutzers hinzu. Dieser Vorgang geschieht automatisch, was dazu führt, dass Administratoren keinen zusätzlichen Archivspeicher anfordern oder die automatisch wachsende Archivierung verwalten müssen. 
  
Hier finden Sie eine kurze Übersicht über den Prozess.
  
![Übersicht über den automatisch expandierenden Archivierungsprozess](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. Die Archivierung ist für ein Benutzerpostfach oder ein freigegebenes Postfach aktiviert. Ein Archivpostfach mit 100 GB Speicherplatz wird erstellt, und das Warnungskontingent für das Archivpostfach ist auf 90 GB festgelegt.
    
2. Ein Administrator ermöglicht die automatische Erweiterung der Archivierung für das Postfach. Wenn das Archivpostfach (einschließlich des Ordners "Wiederherstellbare Elemente") dann 90 GB erreicht, wird es in ein automatisch erweiterbares Archiv konvertiert, und in Office 365 wird dem Archivspeicher Platz hinzugefügt. Beachten Sie, dass es bis zu 30 Tage dauern kann, bis der zusätzliche Speicherplatz bereitgestellt wird.
    
3. Bei Bedarf fügt Office 365 automatisch mehr Speicherplatz zum Archiv hinzu.
  
> [!IMPORTANT]
> Wenn ein Postfach gehalten oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen wird, wird das Speicherkontingent für das Archiv maibox auf 110 GB erhöht, wenn die automatische Erweiterung der Archivierung aktiviert ist. Entsprechend wird das Kontingent für die Archiv Warnung auf 100 GB erhöht.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>Was wird auf den zusätzlichen Archivspeicher Platz verschoben?

Um den automatisch expandierenden Archivspeicher effizient zu nutzen, werden Ordner möglicherweise verschoben. Office 365 bestimmt, welche Ordner verschoben werden, wenn dem Archiv zusätzlicher Speicher hinzugefügt wird. Wenn ein Ordner verschoben wird, wird automatisch ein Unterordner im Archivteil der Ordnerliste in Outlook im ursprünglichen Ordner erstellt. Dieser neue Unterordner verweist auf die Elemente, die verschoben wurden. die benennungskonvention, die Office 365 zum benennen dieses ordners verwendet, ist der ** \<ordner\>name _yyyy (erstellt auf mmm dd, yyyy h_mm)**, wobei folgendes gilt: 
  
- **yyyy** ist das Jahr, in dem die Nachrichten im Ordner empfangen wurden. 
    
- **Mmm dd, yyyy h_m** ist das Datum und die Uhrzeit, zu der der Unterordner von Office 365 im UTC-Format erstellt wurde, basierend auf der Zeitzone des Benutzers und den regionalen Einstellungen in Outlook. 
    
Die folgenden Screenshots zeigen eine Ordnerliste vor und nach dem Verschieben von Nachrichten in einem automatisch erweiterten Archiv.
  
 **Bevor zusätzlicher Speicher hinzugefügt wird**
  
![Ordnerliste des Archivpostfachs vor dem automatischen Erweitern des Archivs](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **Nachdem zusätzlicher Speicher hinzugefügt wurde**
  
![Ordnerliste des Archivpostfachs nach dem automatischen Erweitern des Archivs](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>Outlook-Anforderungen für den Zugriff auf Elemente in einem automatisch erweiterten Archiv

Für den Zugriff auf Nachrichten, die in einem automatisch erweiterten Archiv gespeichert sind, müssen Benutzer einen der folgenden Outlook-Clients verwenden:
  
- Outlook 2016 oder Outlook 2019 für Windows
    
- Outlook im Web 
    
- Outlook 2016 oder Outlook 2019 für Mac 
    
> [!NOTE]
> Outlook 2013-Benutzer können nur auf Elemente zugreifen, die ursprünglich in Ihrem Archivpostfach gespeichert waren. Sie können nicht auf Elemente zugreifen, die in zusätzlichen Archivspeicher verschoben werden. 
  
Bei der Verwendung von Outlook oder Outlook im Web für den Zugriff auf Nachrichten, die in einem automatisch erweiterten Archiv gespeichert sind, sollten Sie Folgendes berücksichtigen.
  
- Sie können auf einen beliebigen Ordner in Ihrem Archivpostfach zugreifen, einschließlich derer, die in den automatisch erweiterten Speicherbereich verschoben wurden.
    
- Sie können nur nach Elementen suchen, die in einen zusätzlichen Speicherbereich verschoben wurden, indem Sie den Ordner selbst durchsuchen. Dies führt dazu, dass Sie den Ordner Archiv in der Ordnerliste auswählen müssen, um die Option **Aktueller Ordner** als Suchbereich auszuwählen. Auch wenn ein Ordner in einem automatisch erweiterten Speicherbereich Unterordner enthält, müssen Sie die einzelnen Unterordnern separat durchsuchen. 
    
- Die Anzahl der Elemente in Outlook und das Lesen/ungelesene zählen (in Outlook und Outlook im Web) in einem automatisch erweiterten Archiv ist möglicherweise nicht korrekt.
    
- Sie können Elemente in einem Unterordner löschen, der auf einen automatisch erweiterten Speicherbereich zeigt, aber der Ordner selbst kann nicht gelöscht werden.
    
- Sie können das Feature Gelöschte Elemente wiederherstellen nicht verwenden, um ein Element wiederherzustellen, das aus einem automatisch erweiterten Speicherbereich gelöscht wurde.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>Automatisches Erweitern von Archivierungs-und anderen Office 365-Kompatibilitätsfeatures

In diesem Abschnitt wird die Funktionalität zwischen der automatischen Erweiterung der Archivierung und anderen Office 365-Kompatibilitäts-und Daten Steuerungsfeatures erläutert.
  
- **eDiscovery** -Wenn Sie ein Office 365 eDiscovery-Tool wie Inhaltssuche oder in-Place eDiscovery verwenden, werden auch die zusätzlichen Speicherbereiche in einem automatisch erweiterten Archiv durchsucht.
    
- **Aufbewahrung** – Wenn Sie ein Postfach mithilfe von Tools wie der Beweissicherung in Exchange Online oder eDiscovery Case Holds und Aufbewahrungsrichtlinien im Office 365 Security _AMP_ Compliance Center halten, werden Inhalte, die sich in einem automatisch erweiterten Archiv befinden, auch in der Warteschleife gehalten.
    
- **Messaging Records Management (MRM)** – Wenn Sie in Exchange Online MRM-Löschrichtlinien verwenden, um abgelaufene Postfachelemente dauerhaft zu löschen, werden auch abgelaufene Elemente im automatisch erweiterten Archiv gelöscht.
    
- **Import Dienst** – Sie können den Office 365-Import Dienst verwenden, um PST-Dateien in das automatisch erweiterte Archiv eines Benutzers zu importieren. Sie können bis zu 100 GB Daten aus PST-Dateien in das Archivpostfach des Benutzers importieren. 

## <a name="more-information"></a>Weitere Informationen

Weitere technische Details zur automatisch expandierenden Archivierung finden Sie unter [Office 365: häufig gestellte Fragen zur automatischen Erweiterung](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/)von Archiven.