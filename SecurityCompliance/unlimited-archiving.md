---
title: Übersicht über die unbegrenzte Archivierung in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
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
description: Erfahren Sie mehr über die automatische Erweiterung der Archivierung in Office 365, die unbegrenzten Archivspeicher für Exchange Online Postfächer bereitstellt.
ms.openlocfilehash: 21489683bbb9f3e2addb5e95a38d8f8a418639de
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231079"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Übersicht über die unbegrenzte Archivierung in Office 365

In Office 365 bieten Archivpostfächer Benutzern zusätzlichen Postfachspeicher Platz. Nachdem das Archivpostfach eines Benutzers aktiviert wurde, ist ein zusätzlicher Speicher von bis zu 100 GB verfügbar. In der Vergangenheit, wenn das Speicherkontingent von 100 GB erreicht wurde, mussten sich Organisationen an Microsoft wenden, um zusätzlichen Speicherplatz für ein Archivpostfach anzufordern. Das ist nicht mehr der Fall.

Das Feature für unbegrenzte Archivierung in Office 365 (als *automatisch expandierende Archivierung*bezeichnet) bietet eine unbegrenzte Menge an Speicherplatz in archivpostfächern. Wenn nun das Speicherkontingent im Archivpostfach erreicht wird, vergrößert Office 365 automatisch die Größe des Archivs, was bedeutet, dass Benutzern kein Postfachspeicher Platz mehr zur Verweilen ist und Administratoren keinen zusätzlichen Speicher für Archivpostfächer anfordern müssen. .
  
Eine Schritt-für-Schritt-Anleitung zum Aktivieren der automatischen Erweiterung der Archivierung finden Sie unter [enable Unlimited Archiving in Office 365](enable-unlimited-archiving.md).
  
> [!NOTE]
> Die Archivierung mit automatischer Erweiterung unterstützt auch freigegebene Postfächer. Um das Archiv für ein freigegebenes Postfach zu aktivieren, ist eine Exchange Online Plan 2-Lizenz oder eine Exchange Onlineplan 1-Lizenz mit einer Exchange Online-Archivierungslizenz erforderlich. 
  
## <a name="how-auto-expanding-archiving-works"></a>Funktionsweise der automatisch expandierenden Archivierung

Wie bereits erläutert, wird zusätzlicher Postfachspeicher Platz erstellt, wenn das Archivpostfach eines Benutzers aktiviert ist. Wenn die automatisch expandierende Archivierung aktiviert ist, überprüft Office 365 regelmäßig die Größe des Archivpostfachs. Wenn ein Archivpostfach seinen Speichergrenzwert erreicht, wird von Office 365 automatisch zusätzlicher Speicherplatz für das Archiv erstellt. Wenn der Benutzer diesen zusätzlichen Speicherplatz ausgibt, fügt Office 365 dem Archiv des Benutzers mehr Speicherplatz hinzu. Dieser Vorgang wird automatisch ausgeführt, was bedeutet, dass Administratoren keinen zusätzlichen Archivspeicher anfordern oder die automatisch erweiterte Archivierung verwalten müssen. 
  
Hier finden Sie eine kurze Übersicht über den Prozess.
  
![Übersicht über den automatisch wachsenden Archivierungsprozess](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. Die Archivierung ist für ein Benutzerpostfach oder ein freigegebenes Postfach aktiviert. Ein Archivpostfach mit 100 GB Speicherplatz wird erstellt, und das Warn Kontingent für das Archivpostfach ist auf 90 GB festgelegt.
    
2. Ein Administrator aktiviert die automatisch erweiterte Archivierung für das Postfach. Wenn das Archivpostfach (einschließlich des Ordners "Wiederherstellbare Elemente") dann 90 GB erreicht, wird es in ein automatisch expandierendes Archiv konvertiert, und Office 365 dem Archivspeicher Platz hinzugefügt. Beachten Sie, dass es bis zu 30 Tage dauern kann, bis der zusätzliche Speicherplatz bereitgestellt wird.
    
3. Bei Bedarf fügt Office 365 dem Archiv automatisch mehr Speicherplatz hinzu.
  
> [!IMPORTANT]
> Wenn ein Postfach gespeichert oder einer Office 365 Aufbewahrungsrichtlinie zugewiesen ist, wird das Speicherkontingent für das Archiv maibox auf 110 GB erhöht, wenn die automatische Erweiterung der Archivierung aktiviert ist. Dementsprechend wird das Kontingent für die Archiv Warnung auf 100 GB erhöht.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>Was wird auf den zusätzlichen Archivspeicherplatz verschoben?

Um den automatisch wachsenden Archivspeicher effizient zu nutzen, werden möglicherweise die Ordner verschoben. Office 365 bestimmt, welche Ordner verschoben werden, wenn dem Archiv zusätzlicher Speicher hinzugefügt wird. Wenn ein Ordner verschoben wird, wird automatisch ein Unterordner unter dem ursprünglichen Ordner im Archivteil der Ordnerliste in Outlook erstellt. Dieser neue Unterordner verweist auf die Elemente, die verschoben wurden. Die Benennungskonvention, die Office 365 zum Benennen dieses Ordners verwendet, ist ** \<Folder\>Name _yyyy (erstellt in Mmm dd, yyyy h_mm)**, wobei Folgendes gilt: 
  
- **yyyy** ist das Jahr, in dem die Nachrichten im Ordner empfangen wurden. 
    
- **mmm tt, yyyy h_m** ist das Datum und die Uhrzeit, zu der der Unterordner von Office 365 im UTC-Format basierend auf der Zeitzone des Benutzers und den regionalen Einstellungen in Outlook erstellt wurde. 
    
Die folgenden Screenshots zeigen eine Ordnerliste vor und nach dem Verschieben von Nachrichten in einem automatisch erweiterten Archiv.
  
 **Bevor zusätzlicher Speicher hinzugefügt wird**
  
![Ordnerliste des Archivpostfachs vor der Einrichtung des automatisch expandierenden Archivs](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **Nachdem zusätzlicher Speicher hinzugefügt wurde**
  
![Ordnerliste des Archivpostfachs, nachdem das Archiv automatisch erweitert wurde](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>Outlook-Anforderungen für den Zugriff auf Elemente in einem automatisch erweiterten Archiv

Für den Zugriff auf Nachrichten, die in einem automatisch erweiterten Archiv gespeichert sind, müssen Benutzer einen der folgenden Outlook-Clients verwenden:
  
- Outlook 2016 oder Outlook 2019 für Windows
    
- Outlook im Web 
    
- Outlook 2016 oder Outlook 2019 für Mac 
    
> [!NOTE]
> Outlook 2013 Benutzer können nur auf Elemente zugreifen, die ursprünglich in Ihrem Archivpostfach gespeichert waren. Sie können nicht auf Elemente zugreifen, die in zusätzlichen Archivspeicher verschoben werden. 
  
Hier sind einige Punkte, die Sie berücksichtigen sollten, wenn Sie Outlook oder Outlook im Internet verwenden, um auf Nachrichten zuzugreifen, die in einem automatisch erweiterten Archiv gespeichert sind.
  
- Sie können auf einen beliebigen Ordner im Archivpostfach zugreifen, einschließlich derer, die in den automatisch erweiterten Speicherbereich verschoben wurden.
    
- Sie können nur nach Elementen suchen, die in einen zusätzlichen Speicherbereich verschoben wurden, indem Sie den Ordner selbst durchsuchen. Dies bedeutet, dass Sie den Archivordner in der Ordnerliste auswählen müssen, um die Option **Aktueller Ordner** als Suchbereich auszuwählen. Wenn ein Ordner in einem automatisch erweiterten Speicherbereich Unterordner enthält, müssen Sie auch jeden Unterordner einzeln durchsuchen. 
    
- Elementanzahlen in Outlook und Lese-/ungelesene Zählungen (in Outlook und Outlook im Web) in einem automatisch erweiterten Archiv sind möglicherweise nicht korrekt.
    
- Sie können Elemente in einem Unterordner löschen, der auf einen automatisch erweiterten Speicherbereich zeigt, aber der Ordner selbst kann nicht gelöscht werden.
    
- Sie können das Feature Gelöschte Elemente wiederherstellen nicht verwenden, um ein Element wiederherzustellen, das aus einem automatisch erweiterten Speicherbereich gelöscht wurde.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>Automatisches Erweitern der Archivierung und anderer Office 365-Kompatibilitätsfeatures

In diesem Abschnitt wird die Funktionalität zwischen der automatisch wachsenden Archivierung und anderen Office 365-Compliance-und Data Governance-Features erläutert.
  
- **eDiscovery** – Wenn Sie ein Office 365 eDiscovery-Tool wie Inhaltssuche oder in-Place-eDiscovery verwenden, werden auch die zusätzlichen Speicherbereiche in einem automatisch erweiterten Archiv durchsucht.
    
- **Aufbewahrung** – Wenn Sie ein Postfach mithilfe von Tools wie Beweissicherungsverfahren in Exchange Online-oder eDiscovery-Fall-und Aufbewahrungsrichtlinien im Security and Compliance Center speichern, wird der Inhalt in einem automatisch erweiterten Archiv ebenfalls aufbewahrt.
    
- **Messaging Records Management (MRM)** – Wenn Sie MRM-Löschrichtlinien in Exchange Online verwenden, um abgelaufene Postfachelemente endgültig zu löschen, werden abgelaufene Elemente, die sich im automatisch erweiterten Archiv befinden, ebenfalls gelöscht.
    
- **Import Dienst** : Sie können den Office 365-Import Dienst verwenden, um PST-Dateien in das automatisch erweiterte Archiv eines Benutzers zu importieren. Sie können bis zu 100 GB Daten aus PST-Dateien in das Archivpostfach des Benutzers importieren. 

## <a name="more-information"></a>Weitere Informationen

Weitere technische Details zur automatischen Erweiterung der Archivierung finden Sie unter [Office 365: häufig gestellte Fragen zum automatischen erweitern](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/)von Archiven.