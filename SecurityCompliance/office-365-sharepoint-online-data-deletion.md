---
title: Office 365 SharePoint Online-Daten löschen
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
description: Eine Erläuterung der Löschung von Daten in SharePoint Online.
ms.openlocfilehash: 97f3eaea471c08ba61c0fc749b806c1960c0182f
ms.sourcegitcommit: ee1d7037d9ad14d7f0dbc53114177a3d04614d6e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25402039"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a>SharePoint Online-Daten löschen in Office 365

SharePoint Online werden Objekte als abstrahiert Code in Datenbanken gespeichert. Wenn ein Benutzer eine Datei mit SharePoint Online hochgeladen wird, wird diese Datei zerlegt und in der Anwendungscode übersetzt und in mehreren Tabellen in mehreren Datenbanken gespeichert. Alle Inhalte, die ein Kunde hochlädt ist in SharePoint Online-Segmenten verschlüsselt (potenziell mit mehreren AES 256-Bit-Schlüssel), aufgeschlüsselt und Datencenter verteilt. Ausführliche Informationen zum Prozess Segmentierung und Verschlüsselung finden Sie unter [Verschlüsselung in der Microsoft-Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md). Datenschutz-Services werden bereitgestellt, um den Verlust von SharePoint Online-Daten zu verhindern. Insbesondere sind Sicherungen ausgeführt alle 12 Stunden und 14 Tage lang aufbewahrt.

Wenn Sie Inhalte aus einer SharePoint Online-Website löschen, wird es nicht sofort gelöscht. Es wird gesendet in einer Website Papierkorb, wobei es wiederhergestellt werden kann, falls erforderlich. (Schritte zur Wiederherstellung finden Sie unter [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) .) Die Standardeinstellung Website Papierkorb Retention ist etwa 90 Tage. Wenn Sie Inhalte aus einer Website Papierkorb löschen, wird sie in den Papierkorb der Website gesendet, die eine Aufbewahrungszeit 93 Tage hat. Die Zeitdauer in den Papierkorb garantiert kann von einem Administrator konfiguriert werden, aber keine, die Aufbewahrungsdauer standardmäßig etwa 90 Tage ist. Die Recycle Bin Websitespeicher wirkt sich nachteilig auf die Website-Auflistung von Speicherkontingenten und den [Schwellenwert für die Listenansicht](https://support.office.com/article/List-View-Threshold-b8588dae-9387-48c2-9248-c24122f07c59).

Wenn Sie eine Websitesammlung löschen, können Sie auch die Hierarchie der Websites in der Auflistung, einschließlich Informationen für alle Inhalte und Benutzerinformationen löschen:
- Dokumente und Dokumentbibliotheken
- Listen und Listendaten
- Einstellungen für die Websitekonfiguration
- Rolle und Sicherheitsinformationen Informationen, die auf der Website oder Unterwebsites zusammenhängt
- Unterwebsites der Website, deren Inhalt und Benutzer auf oberster Ebene Informationen

Bevor Sie eine Websitesammlung löschen, wird empfohlen, dass Sie die SharePoint Online-Dienstbeschreibung für den Plan überprüfen, die Daten Sicherungszeitplan für SharePoint Online-Websites von Microsoft verwaltet werden. Auch Notiz, die Wiederherstellungen aus Sicherungen können nur für Websitesammlungen oder Unterwebsites nicht für Dateien, Listen oder Bibliotheken sind. Wenn Sie diese wiederherstellen müssen, verwenden Sie den Papierkorb. Wenn Sie eine Websitesammlung versehentlich gelöscht haben, können sie aus den Papierkorb der Websitesammlung durch ein Websitesammlungsadministrator innerhalb von 93 Tagen wiederhergestellt werden.

Festplatte Löschvorgang tritt auf, wenn ein Benutzer löscht gelöschte Elemente aus dem Papierkorb für die Website ein, und die Archivierung und backup-Zeitfenster laufen ab, oder wenn ein Administrator eine Websitesammlung mit dem [Remove-SPODeletedSite-Cmdlet](https://docs.microsoft.com/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)dauerhaft gelöscht. Wenn ein harte Benutzer löscht (dauerhaft gelöscht oder löscht) Inhalte aus SharePoint Online, alle Verschlüsselungsschlüssel für die gelöschten Blöcke werden ebenfalls gelöscht. Die Blöcke auf den Datenträgern, die die gelöschten Blöcke zuvor gespeichert werden als nicht verwendete und bereit zur Wiederverwendung gekennzeichnet.
