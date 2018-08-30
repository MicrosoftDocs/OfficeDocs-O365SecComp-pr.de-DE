---
title: Office 365 SharePoint-Daten Resiliency
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine Übersicht über die ausfallsicherheit von Daten in SharePoint Online in Office 365.
ms.openlocfilehash: ba6259e8e582a4abcf0f184b162177119a57718f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529452"
---
# <a name="sharepoint-online-data-resiliency"></a>SharePoint Online-Datenflexibilität
Ein zentrales Prinzip für SharePoint Online ist noch nie eine einzelne Kopie beliebiger Daten. SharePoint Online arbeitet mit SQL Server-Replikation, eine Reihe von Technologien zum Kopieren und Verteilen von Daten und Datenbankobjekten aus einer Datenbank in eine andere, und klicken Sie dann die Synchronisierung zwischen Datenbanken zum Aufrechterhalten der Konsistenz. 

Beispielsweise wenn ein Benutzer eine Datei in SharePoint Online speichert, ist die Datei chunked verschlüsselt und in Azure BLOB-Speicher gespeichert. Azure BLOB-Dienst bietet Mechanismen beide auf den Ebenen Anwendung und Transport Sicherstellung der Datenintegrität. Dieser Beitrag wird diese Mechanismen aus der Sicht Service und -Client beschrieben. Überprüfung der MD5 ist optional auf PUT und GET-Prozesse. Es wird jedoch eine benutzerfreundliche Funktion, die Sicherstellung der Datenintegrität über das Netzwerk bei Verwendung von HTTP bereitgestellt. Darüber hinaus seit HTTPS Transport Layer Security zusätzliche enthält MD5 Überprüfung ist nicht erforderlich, beim Herstellen einer Verbindung über HTTPS, wie sie redundante wäre. Azure Blob-Dienst bietet eine dauerhafte Speichermedium und einen eigenen integritätsprüfung für gespeicherte Daten verwendet. MD5s, die verwendet werden, wenn für die Interaktion mit einer Anwendung dienen zum Überprüfen der Integrität der Daten, wenn diese Daten zwischen der Anwendung und dem über HTTP zu übertragen. 

Um den Azure Blob Sicherstellung der Datenintegrität verwendet Service MD5-Hashwerte der Daten in einige Arten implementiert. Es ist wichtig zu verstehen, wie diese Werte werden berechnet, übertragen, gespeichert und schließlich erzwungen wird, um entsprechend Entwerfen der Anwendung verwenden, um die Datenintegrität bereitzustellen. Weitere Informationen finden Sie unter [Windows Azure Blob MD5 (Übersicht)](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx). 

Metadaten sowie Zeiger auf die Datei werden in einer SQL Server-Datenbank (die Content-Datenbank) gespeichert. Die Blöcke – Dateien, Dateien und Update Deltas – werden als Blobs in Azure-Speicher gespeichert, die über mehrere Konten der Azure-Speicher nach dem Zufallsprinzip verteilt werden. Die SQL-Datenbank ist auf einem Speicher-Array für RAID 10 gehostet, das an ein anderes Array von RAID 10 Speicher in einem separaten Racks im selben Rechenzentrum synchron gespiegelt wird. Asynchrone Protokollversand wird zum Replizieren von Daten an ein anderes Array von RAID 10 Speicher in einem zweiten Rechenzentrum verwendet. Zusätzlich zum Schutz von Daten mit RAID 10 und synchrone und asynchrone Replikation stammen geplanten datensicherungen die in der zweiten Datencenter auch asynchron repliziert werden. 

Daten gesichert werden in SharePoint Online – alle 12 Stunden ausgeführt und 14 Tage lang aufbewahrt. SharePoint Online verwendet auch hot standby-System, die enthält gekoppelten geografisch getrennte Rechenzentren innerhalb der gleichen Kunden Daten Speicherort Region (beispielsweise "Chicago" und San Andreas für Kunden, die mit der Bereitstellung ihrer Mandanten in den USA) als aktiv/aktiv konfiguriert ist. Es sind beispielsweise live Benutzer, die "Chicago" als ihre primären Datencenter und San Andreas als ein Failover Datencenter und live-Benutzern, die ihre primären Datencenter und Chicago als Rechenzentrum Failover San Andreas verfügen. 