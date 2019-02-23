---
title: Office 365 SharePoint-Datenausfall Sicherheit
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Übersicht über die Datensicherheit in SharePoint Online in Office 365.
ms.openlocfilehash: 4fd17b50551639f6e11975acbc3822fb6ffa8bb2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214805"
---
# <a name="sharepoint-online-data-resiliency"></a>SharePoint Online-Datensicherheit
Ein zentrales Prinzip für SharePoint Online besteht darin, nie eine einzelne Kopie eines Datenteils zu haben. SharePoint Online verwendet die SQL Server-Replikation, bei der es sich um eine Reihe von Technologien für das Kopieren und Verteilen von Daten und Datenbankobjekten aus einer Datenbank in eine andere handelt und die anschließende Synchronisierung zwischen Datenbanken, um die Konsistenz zu gewährleisten. 

Wenn ein Benutzer beispielsweise eine Datei in SharePoint Online speichert, wird die Datei segmentiert, verschlüsselt und innerhalb des Azure-BLOB-Speichers gespeichert. Der Azure-BLOB-Dienst bietet Mechanismen zur Sicherstellung der Datenintegrität sowohl auf Anwendungs-als auch Transportebenen. In diesem Beitrag werden diese Mechanismen aus der Dienst-und Clientperspektive detailliert beschrieben. Die MD5-Überprüfung ist für PUT-und GET-Vorgänge optional; Sie bietet jedoch eine einfache Möglichkeit, die Datenintegrität im gesamten Netzwerk bei Verwendung von HTTP sicherzustellen. Da HTTPS eine Transportschichtsicherheit bietet, ist zusätzlich eine MD5-Überprüfung bei der Verbindung über HTTPS nicht erforderlich, da dies redundant wäre. Der Azure-BLOB-Dienst stellt ein dauerhaftes Speichermedium bereit und verwendet seine eigene Integritätsprüfung für gespeicherte Daten. Die MD5's, die bei der Interaktion mit einer Anwendung verwendet werden, werden zur Überprüfung der Integrität der Daten bei der Übertragung dieser Daten zwischen der Anwendung und dem Dienst über HTTP bereitgestellt. 

Zur Sicherstellung der Datenintegrität verwendet der Azure-BLOB-Dienst MD5-Hashes der Daten auf ein paar verschiedene Arten. Es ist wichtig zu verstehen, wie diese Werte berechnet, übermittelt, gespeichert und schließlich erzwungen werden, um Ihre Anwendung entsprechend zu entwerfen, um die Datenintegrität zu gewährleisten. Weitere Informationen finden Sie unter [Windows Azure BLOB MD5 Overview](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx). 

Metadaten und Zeiger auf die Datei werden in einer SQL Server-Datenbank (der Inhaltsdatenbank) gespeichert. Alle Chunks – Dateien, Dateien und Update-Deltas – werden als BLOBs im Azure-Speicher gespeichert, die nach dem Zufallsprinzip über mehrere Azure-Speicherkonten verteilt werden. Die SQL-Datenbank wird in einem RAID 10-Speicherarray gehostet, das synchron zu einem anderen RAID 10-Speicherarray in einem separaten Rack innerhalb desselben Datencenters gespiegelt wird. Der asynchrone Protokollversand wird dann zum Replizieren der Daten in ein anderes RAID 10-Speicherarray in einem zweiten Rechenzentrum verwendet. Zusätzlich zum Schutz von Daten mit RAID 10 und synchroner und asynchroner Replikation werden geplante Datensicherungen ausgeführt, die ebenfalls asynchron in das zweite Rechenzentrum repliziert werden. 

In SharePoint Online werden Datensicherungen alle 12 Stunden durchgeführt und für 14 Tage aufbewahrt. SharePoint Online verwendet außerdem ein betriebsbereites Standbysystem, das paarweise geografisch getrennte Rechenzentren innerhalb derselben Kundendaten-Standort Region (beispielsweise Chicago und San Antonio für Kunden, die ihren Mandanten in den USA bereitgestellt haben) umfasst. als aktiv/aktiv konfiguriert. Beispielsweise gibt es Live-Benutzer, die Chicago als primäres Datencenter und San Antonio als Failover-Datencenter und Live-Benutzer mit San Antonio als primärem Datencenter und Chicago als Failover-Datencenter haben. 