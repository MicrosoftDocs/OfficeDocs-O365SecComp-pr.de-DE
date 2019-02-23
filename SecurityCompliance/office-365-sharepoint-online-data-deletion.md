---
title: Office 365 SharePoint Online-Datenlöschung
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Erklärung zum Löschen von Daten in SharePoint Online.
ms.openlocfilehash: 6d4989bc4b503309ba50237a164bffebaff1e7af
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218425"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a>Löschen von SharePoint Online-Daten in Office 365

SharePoint Online speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer eine Datei in SharePoint Online hochlädt, wird diese Datei zerlegt und in Anwendungscode übersetzt und in mehreren Tabellen über mehrere Datenbanken gespeichert. In SharePoint Online werden alle Inhalte, die ein Kunde hochlädt, in Abschnitte unterteilt, verschlüsselt (potenziell mit mehreren AES 256-Bit-Schlüsseln) und über das Datencenter verteilt. Ausführliche Informationen zum Chunking-und Verschlüsselungsprozess finden Sie unter [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md). 

In SharePoint Online werden Elemente 93 Tage lang aufbewahrt, ab dem Zeitpunkt, zu dem Sie Sie vom ursprünglichen Speicherort gelöscht haben. Sie bleiben die gesamte Zeit im Papierkorb der Website, es sei denn, Sie werden von dort gelöscht oder geleert. In diesem Fall gehen die Elemente in den Papierkorb der Websitesammlung, in dem Sie für den Rest der 93 Tage verbleiben. Informationen zum Wiederherstellen gelöschter Elemente finden Sie unter [Wiederherstellen von Elementen im Papierkorb einer SharePoint-Website](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) und [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). Die Aufbewahrungszeit des Papierkorbs kann in SharePoint Online nicht konfiguriert werden.

Wenn Sie eine Websitesammlung löschen, löschen Sie auch die Hierarchie der Websites in der Auflistung und alle darin enthaltenen Inhalte:
- Dokumente und Dokumentbibliotheken
- Listen und Auflisten von Daten
- Website Konfigurationseinstellungen
- Rollen-und Sicherheitsinformationen im Zusammenhang mit der Website oder ihren Unterwebsites
- Unterwebsites der Website auf höchster Ebene, deren Inhalte und Benutzerinformationen

Wenn Sie eine Websitesammlung versehentlich löschen, kann Sie von einem globalen oder SharePoint-Administrator mithilfe des SharePoint admin Centers wiederhergestellt werden. 

Das harte löschen tritt auf, wenn ein Benutzer gelöschte Elemente aus dem Papierkorb der Websitesammlung löscht, wenn die Aufbewahrungs-und Sicherungs Zeiträume abgelaufen sind oder wenn ein Administrator eine Websitesammlung mithilfe des [Remove-SPODeletedSite-Cmdlets](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps)dauerhaft gelöscht. Wenn ein Benutzer Inhalte aus SharePoint Online löscht (dauerhaft gelöscht oder löscht), werden auch alle Verschlüsselungsschlüssel für die gelöschten Chunks gelöscht. Die Blöcke auf den Datenträgern, die zuvor die gelöschten Chunks gespeichert haben, werden als nicht verwendet markiert und können wieder verwendet werden.
