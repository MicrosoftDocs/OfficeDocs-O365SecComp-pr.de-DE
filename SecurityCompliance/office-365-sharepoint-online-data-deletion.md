---
title: Office 365 SharePoint Online-Daten löschen
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine Erläuterung der Löschung von Daten in SharePoint Online.
ms.openlocfilehash: 8a84859ce170a4c3ca713c751aef2b6d5b911c55
ms.sourcegitcommit: 29ba4c36af8e90ddc8d885863ef25bac2cffbe94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2018
ms.locfileid: "27411161"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a>SharePoint Online-Daten löschen in Office 365

SharePoint Online werden Objekte als abstrahiert Code in Datenbanken gespeichert. Wenn ein Benutzer eine Datei mit SharePoint Online hochgeladen wird, wird diese Datei zerlegt und in der Anwendungscode übersetzt und in mehreren Tabellen in mehreren Datenbanken gespeichert. Alle Inhalte, die ein Kunde hochlädt ist in SharePoint Online-Segmenten verschlüsselt (potenziell mit mehreren AES 256-Bit-Schlüssel), aufgeschlüsselt und Datencenter verteilt. Ausführliche Informationen zum Prozess Segmentierung und Verschlüsselung finden Sie unter [Verschlüsselung in der Microsoft-Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md). 

In SharePoint Online – werden Elemente für 93 Tagen ab dem Zeitpunkt beibehalten, die Sie sie aus dem ursprünglichen Speicherort löschen. Sie bleiben im Papierkorb der Website die gesamte Zeit, es sei denn, ein Benutzer löscht diese dann von dort aus oder, Papierkorb Leert. In diesem Fall werden die Elemente der Websitesammlung Papierkorb, wobei sie für den Rest der 93 Tage bleiben. Informationen zum Wiederherstellen von gelöschten Elementen finden Sie unter [Wiederherstellen von Elementen im Papierkorb der SharePoint-Website](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) und [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). Die Aufbewahrungszeit Recycle Bin ist nicht konfigurierbar in SharePoint Online.

Wenn Sie eine Websitesammlung löschen, sind Sie auch die Hierarchie der Websites in der Auflistung und alle Inhalte zu löschen:
- Dokumente und Dokumentbibliotheken
- Listen und Listendaten
- Einstellungen für die Websitekonfiguration
- Rolle und Sicherheitsinformationen Informationen, die auf der Website oder Unterwebsites zusammenhängt
- Unterwebsites der Website, deren Inhalt und Benutzer auf oberster Ebene Informationen

Wenn Sie eine Websitesammlung versehentlich gelöscht haben, können sie durch ein globaler oder SharePoint wiederhergestellt Admin mit der SharePoint-Verwaltungskonsole. 

Festplatte Löschvorgang tritt auf, wenn ein Benutzer gelöschte Elemente aus der Websitesammlung des Papierkorbs löscht, wenn die Archivierung und Sicherung Perioden ablaufen oder ein Administrator eine Websitesammlung mit dem [Remove-SPODeletedSite-Cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)dauerhaft gelöscht. Wenn ein harte Benutzer löscht (dauerhaft gelöscht oder löscht) Inhalte aus SharePoint Online, alle Verschlüsselungsschlüssel für die gelöschten Blöcke werden ebenfalls gelöscht. Die Blöcke auf den Datenträgern, die die gelöschten Blöcke zuvor gespeichert werden als nicht verwendete und bereit zur Wiederverwendung gekennzeichnet.
